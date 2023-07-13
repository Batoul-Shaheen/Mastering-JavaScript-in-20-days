# Day 10: 💻

**Asynchronous JavaScript & the event loop**

## Lesson Summary:

#### Asynchronous 
Tackles tasks that take time to complete like :
- fetching data from server.
- reading file.

there are several ways to achieve async:
1. callback function.
2. Promises.
3. async/await syntax.


#### Promises
Benefits
- Cleaner readable style with pseudo-synchronous style code.
- Nice error handling process.
- `.then` -> reslove.
- `.catch` -> reject.

## Challenges:
### [Questions](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/146299d463da8ad3a5dfeb926ad8153c2c6a11bd/learning-sprint-1/week2-day3-tasks/tasks.md)

#### Question 1:
#### my solution:

```javascript
const executeInSequenceWithCBs = (tasks, callback) => {
  const messages = [];

  const executeTask = async (task) => {
    return new Promise((resolve) => {
      task((message) => {
        messages.push(message);
        resolve();
      });
    });
  };

  const executeTasks = async () => {
    for (const task of tasks) {
      await executeTask(task);
    }

    callback(messages);
  };

  executeTasks();
};

executeInSequenceWithCBs(asyncTasks, (messages) => {
  console.log(messages);
});
```

#### Question 2:
#### my solution

```javascript
const executeInParallelWithPromises = (apis) => {
  const promises = apis.map(api => fetch(api.apiUrl)
    .then(response => response.json())
    .then(apiData => ({ apiName: api.apiName, apiUrl: api.apiUrl, apiData }))
  );

  return Promise.all(promises);
};

executeInParallelWithPromises(apis)
  .then(results => {
    console.log(results);
  })
  .catch(error => {
    console.error(error);
  });
```

#### Question 3:
#### my solution

```javascript
const executeInSequenceWithPromises = async (apis) => {
  const results = [];

  for (const api of apis) {
    try {
      const response = await fetch(api.apiUrl);
      const apiData = await response.json();

      results.push({
        apiName: api.apiName,
        apiUrl: api.apiUrl,
        apiData: apiData
      });
    } catch (error) {
      console.error(`Error fetching data from ${api.apiName}: ${error}`);
    }
  }

  return results;
};

executeInSequenceWithPromises(apis)
  .then(results => {
    console.log(results);
  })
  .catch(error => {
    console.error(error);
  });
```
