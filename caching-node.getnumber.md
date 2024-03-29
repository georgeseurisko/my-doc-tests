<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@eurisko/caching-node](./caching-node.md) &gt; [getNumber](./caching-node.getnumber.md)

## getNumber variable

A function that returns the value of a key from the namespace of the client, if not found, then generate a value from the passed callback, save it to redis and return it

**Signature:**

```typescript
getNumber: (clientId: string, key: string, callback: Function, ttl?: number) => Promise<number>
```

## Example

//example 1 (key value found) const result = await getNumber('client1', 'key1', () =<!-- -->&gt; 10); console.log(result) // prints 15 found in the namespace of the client on the redis server //example 2 (key value not found, don't add ttl) const result = await getNumber('client1', 'invalidKey', () =<!-- -->&gt; 10); console.log(result) // prints 10 and saves the the key and value pair to the namespace of the client on the redis server //example 3 (key value not found, add ttl) const result = await getNumber('client1', 'invalidKey', () =<!-- -->&gt; 10, 3600); console.log(result) // prints 10 and saves the the key and value pair to the namespace of the client on the redis server with a time to live of 1 hour

