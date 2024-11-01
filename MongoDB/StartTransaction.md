
you can also perform multi-document transactions. Here's how you can do it step-by-step:

1. **Start a Session**: You need to start a session to use transactions.
2. **Start a Transaction**: Use the session to start a transaction.
3. **Perform Operations**: Execute your CRUD operations within the context of the transaction.
4. **Commit the Transaction**: Commit the transaction to apply the changes.
5. **Abort the Transaction**: If needed, abort the transaction to discard the changes.

```js
const session = db.getMongo().startSession();

session.startTransaction();

session.commitTransaction();

session.abortTransaction();
```

```js
const session = client.startSession();

session.startTransaction();

try {
  // Perform multiple operations within the transaction
  await collection1.updateOne({ _id: 123 }, { $set: { balance: 100 } });
  await collection2.updateOne({ _id: 456 }, { $set: { balance: 200 } });

  // If all operations succeed, commit the transaction
  await session.commitTransaction();
} catch (error) {
  // Handle errors and roll back the transaction
  await session.abortTransaction();
} finally {
  // End the session
  session.endSession();
}
```