# AMX ID

For help adding this module, please contact [info@amxdt.net](info@amxdt.net).

### Prebid Configuration

You can configure this module in your `userSync.userIds[]` configuration:

```javascript
pbjs.setConfig({
  userSync: {
    userIds: [
      {
        name: "amxId",
        storage: {
          name: "amxId",
          type: "html5",
          expires: 14,
        },
        params: {
          tagId: "cHJlYmlkLm9yZw",
        },
      },
    ],
  },
});
```

| Param under `userSync.userIds[]` | Scope    | Type   | Description                 | Example                                   |
| -------------------------------- | -------- | ------ | --------------------------- | ----------------------------------------- |
| name                             | Required | string | ID for the amxId module     | `"amxId"`                                 |
| storage                          | Required | Object | Settings for amxId storage  | See [storage settings](#storage-settings) |
| params                           | Optional | Object | Parameters for amxId module | See [params](#params)                     |

### Storage Settings

The following settings are available for the `storage` property in the `userSync.userIds[]` object:

| Param under `storage` | Scope    | Type         | Description                                                                      | Example   |
| --------------------- | -------- | ------------ | -------------------------------------------------------------------------------- | --------- |
| name                  | Required | String       | Where the ID will be stored                                                      | `"amxId"` |
| type                  | Required | String       | This must be `"html5"`                                                           | `"html5"` |
| expires               | Required | Number <= 30 | number of days until the stored ID expires. **Must be less than or equal to 30** | `14`      |
