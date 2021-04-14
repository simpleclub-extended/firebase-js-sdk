<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@firebase/database](./database.md) &gt; [refFromURL](./database.reffromurl.md)

## refFromURL() function

Returns a `Reference` representing the location in the Database corresponding to the provided Firebase URL.

An exception is thrown if the URL is not a valid Firebase Database URL or it has a different domain than the current `Database` instance.

Note that all query parameters (`orderBy`<!-- -->, `limitToLast`<!-- -->, etc.) are ignored and are not applied to the returned `Reference`<!-- -->.

<b>Signature:</b>

```typescript
export declare function refFromURL(db: FirebaseDatabase, url: string): Reference;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  db | [FirebaseDatabase](./database.firebasedatabase.md) | The database instance to obtain a reference for. |
|  url | string | The Firebase URL at which the returned <code>Reference</code> will point. |

<b>Returns:</b>

[Reference](./database.reference.md)

A `Reference` pointing to the provided Firebase URL.
