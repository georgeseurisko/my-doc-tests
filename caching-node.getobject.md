<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@eurisko/caching-node](./caching-node.md) &gt; [getObject](./caching-node.getobject.md)

## getObject variable

A function that returns the value of a key from the namespace of the client, if not found, then generate a value from the passed callback, save it to redis and return it

**Signature:**

```typescript
getObject: (clientId: string, key: string, callback: Function, ttl?: number) => Promise<string | null>
```

## Example

//example 1 (key value found) const result = await getObject('client1', 'key1', () =<!-- -->&gt; { return {<!-- -->innerkey: 'generatedValue'<!-- -->}<!-- -->}<!-- -->); console.log(result) // prints {<!-- -->somekey: 'keyValue1'<!-- -->} found in the namespace of the client on the redis server //example 2 (key value not found, don't add ttl) const result = await getObject('client1', 'invalidKey', () =<!-- -->&gt; {<!-- -->return {<!-- -->innerkey: 'generatedValue'<!-- -->}<!-- -->}<!-- -->); console.log(result) // prints {<!-- -->innerkey: 'generatedValue'<!-- -->} and saves the the key and value pair to the namespace of the client on the redis server //example 3 (key value not found, add ttl) const result = await getObject('client1', 'invalidKey', () =<!-- -->&gt; 'generatedValue', 3600); console.log(result) // prints {<!-- -->innerkey: 'generatedValue'<!-- -->} and saves the the key and value pair to the namespace of the client on the redis server with a time to live of 1 hour

