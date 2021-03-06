<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@firebase/auth](./auth.md) &gt; [verifyBeforeUpdateEmail](./auth.verifybeforeupdateemail.md)

## verifyBeforeUpdateEmail() function

Sends a verification email to a new email address.

<b>Signature:</b>

```typescript
export declare function verifyBeforeUpdateEmail(user: User, newEmail: string, actionCodeSettings?: ActionCodeSettings | null): Promise<void>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  user | [User](./auth.user.md) | The user. |
|  newEmail | string | The new email address to be verified before update. |
|  actionCodeSettings | [ActionCodeSettings](./auth.actioncodesettings.md) \| null | The [ActionCodeSettings](./auth.actioncodesettings.md)<!-- -->. |

<b>Returns:</b>

Promise&lt;void&gt;

## Remarks

The user's email will be updated to the new one after being verified.

If you have a custom email action handler, you can complete the verification process by calling [applyActionCode()](./auth.applyactioncode.md)<!-- -->.

## Example


```javascript
const actionCodeSettings = {
  url: 'https://www.example.com/?email=user@example.com',
  iOS: {
     bundleId: 'com.example.ios'
  },
  android: {
    packageName: 'com.example.android',
    installApp: true,
    minimumVersion: '12'
  },
  handleCodeInApp: true
};
await verifyBeforeUpdateEmail(user, 'newemail@example.com', actionCodeSettings);
// Obtain code from the user.
await applyActionCode(auth, code);

```

