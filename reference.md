# Reference
## Account
<details><summary><code>client.account.<a href="/src/api/resources/account/client/Client.ts">getAccount</a>() -> BrevoApi.GetAccountResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves details of your Brevo account.

**Use this to:**
- Get account information (email, name, company, address)
- Check plan details (type, credits, expiration)
- Get relay information (for transactional emails)
- Check Marketing Automation status
- View date/time preferences and account settings
- Access organization and user identifiers

**Key information returned:**
- Complete account details (organization ID, user ID, company information)
- Address and contact information
- Plan configurations and credit allocations across different verticals
- Marketing Automation settings and tracker key
- SMTP relay configuration for transactional emails
- Date/time preferences and account settings
- Enterprise features availability status

**Important considerations:**
- Provides comprehensive account overview for billing and configuration management
- Essential for understanding current plan limitations and feature availability
- Marketing Automation key required for advanced automation features
- Plan verticals show detailed breakdown across Marketing, Chat, and CRM categories
- Relay configuration crucial for transactional email setup and deliverability
- Date/time preferences affect campaign scheduling and reporting displays
- Enterprise status determines access to advanced features and sub-account management
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.account.getAccount();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `AccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.account.<a href="/src/api/resources/account/client/Client.ts">getAccountActivity</a>({ ...params }) -> BrevoApi.GetAccountActivityResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves user activity logs from your organization for security monitoring and audit compliance.

Use this to:
- Monitor user login activities and access patterns
- Track account modifications and configuration changes
- Generate security audit reports and compliance documentation
- Investigate suspicious activities and unauthorized access
- Monitor team member actions and account usage

Key information returned:
- Complete user activity details and timestamps
- User identification (email, IP address, browser)
- Action types and activity descriptions
- Security-relevant events and access logs
- Historical activity data for audit trails

Note: Requires Enterprise plan for access to organization activity logs.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.account.getAccountActivity();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetAccountActivityRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## MasterAccount
<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">createANewGroupOfSubAccounts</a>({ ...params }) -> BrevoApi.PostCorporateGroupResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint allows to create a group of sub-accounts
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.createANewGroupOfSubAccounts({
    groupName: "My group"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCorporateGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">deleteSubAccountFromGroup</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint allows you to remove a sub-organization from a group.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.deleteSubAccountFromGroup({
    groupId: "groupId",
    subAccountIds: [423432, 234323, 87678]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutCorporateGroupUnlinkGroupIdSubAccountsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">getAGroupDetails</a>({ ...params }) -> BrevoApi.GetCorporateGroupIdResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint allows you to retrieve a specific group’s information such as
the list of sub-organizations and the user associated with the group.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.getAGroupDetails({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCorporateGroupIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">updateAGroupOfSubAccounts</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint allows to update a group of sub-accounts
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.updateAGroupOfSubAccounts({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutCorporateGroupIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">deleteAGroup</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint allows you to delete a group of sub-organizations. When a
group is deleted, the sub-organizations are no longer part of this group.
The users associated with the group are no longer associated with the group
once deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.deleteAGroup({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteCorporateGroupIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">getSubAccountGroups</a>() -> BrevoApi.GetSubAccountGroupsResponseItem[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint allows you to list all groups created on your Admin account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.getSubAccountGroups();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">getCorporateInvitedUsersList</a>({ ...params }) -> BrevoApi.GetCorporateInvitedUsersListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint allows you to list all Admin users of your Admin account. You
can filter users by type (active or pending) and paginate results using
offset and limit.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.getCorporateInvitedUsersList();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCorporateInvitedUsersListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">listOfAllIPs</a>() -> BrevoApi.GetCorporateIpResponseItem[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint allows you to retrieve the list of active IPs on your Admin
account
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.listOfAllIPs();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">getTheDetailsOfRequestedMasterAccount</a>() -> BrevoApi.GetCorporateMasterAccountResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will provide the details of the master account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.getTheDetailsOfRequestedMasterAccount();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">generateSsoTokenToAccessAdminAccount</a>({ ...params }) -> BrevoApi.GetSsoToken</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint generates an SSO token to authenticate and access the admin
account using the endpoint
https://account-app.brevo.com/account/login/corporate/sso/[token], where
[token] will be replaced by the actual token.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.generateSsoTokenToAccessAdminAccount({
    email: "vipin+ent-user@brevo.com"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCorporateSsoTokenRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">getTheListOfAllTheSubAccountsOfTheMasterAccount</a>({ ...params }) -> BrevoApi.GetCorporateSubAccountResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will provide the list all the sub-accounts of the master
account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.getTheListOfAllTheSubAccountsOfTheMasterAccount({
    offset: 1,
    limit: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCorporateSubAccountRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">createANewSubAccountUnderAMasterAccount</a>({ ...params }) -> BrevoApi.PostCorporateSubAccountResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will create a new sub-account under a master account
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.createANewSubAccountUnderAMasterAccount({
    companyName: "Test Sub-account",
    email: "test-sub@example.com",
    groupIds: ["5f8f8c3b5f56a02d4433b3a7", "5f8f8c3b5f56a02d4433b3a8"],
    language: "fr",
    timezone: "Europe/Paris"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCorporateSubAccountRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">associateAnIpToSubAccounts</a>({ ...params }) -> Record&lt;string, unknown&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint allows to associate an IP to sub-accounts
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.associateAnIpToSubAccounts({
    ids: [234322, 325553, 893432],
    ip: "103.11.32.88"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCorporateSubAccountIpAssociateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">dissociateAnIpToSubAccounts</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint allows to dissociate an IP from sub-accounts
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.dissociateAnIpToSubAccounts({
    ids: [234322, 325553, 893432],
    ip: "103.11.32.88"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutCorporateSubAccountIpDissociateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">createAnApiKeyForASubAccount</a>({ ...params }) -> BrevoApi.PostCorporateSubAccountKeyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will generate an API v3 key for a sub-account
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.createAnApiKeyForASubAccount({
    id: 3232323,
    name: "My Api Key"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCorporateSubAccountKeyRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">generateSsoTokenToAccessSubAccount</a>({ ...params }) -> BrevoApi.GetSsoToken</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint generates an sso token to authenticate and access a
sub-account of the master using the account endpoint
https://account-app.brevo.com/account/login/sub-account/sso/[token], where
[token] will be replaced by the actual token.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.generateSsoTokenToAccessSubAccount({
    id: 3232323
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCorporateSubAccountSsoTokenRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">getSubAccountDetails</a>({ ...params }) -> BrevoApi.GetCorporateSubAccountIdResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will provide the details for the specified sub-account company
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.getSubAccountDetails({
    id: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCorporateSubAccountIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">deleteASubAccount</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.deleteASubAccount({
    id: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteCorporateSubAccountIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">enableDisableSubAccountApplicationS</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

API endpoint for the Corporate owner to enable/disable applications on the
sub-account
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.enableDisableSubAccountApplicationS({
    id: 1000000,
    "landing-pages": true,
    meetings: true,
    "sms-campaigns": false,
    "web-push": false,
    whatsapp: true
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutCorporateSubAccountIdApplicationsToggleRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">updateSubAccountPlan</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will update the sub-account plan. On the Corporate solution
new version v2, you can set an unlimited number of credits in your
sub-organization. Please pass the value “-1" to set the consumable in
unlimited mode.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.updateSubAccountPlan({
    id: 1000000,
    credits: {
        email: 5000,
        externalFeeds: 1,
        sms: 2000,
        whatsapp: 100,
        wpSubscribers: -1
    },
    features: {
        inbox: 10,
        landingPage: 20,
        salesUsers: 6,
        users: 15
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutCorporateSubAccountIdPlanRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">updateSubAccountsPlan</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will update multiple sub-accounts plan. On the Corporate
solution new version v2, you can set an unlimited number of credits in your
sub-organization. Please pass the value “-1" to set the consumable in
unlimited mode.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.updateSubAccountsPlan({
    credits: {
        email: 5000,
        externalFeeds: 1,
        sms: 2000,
        whatsapp: 100,
        wpSubscribers: -1
    },
    features: {
        landingPage: 20,
        salesUsers: 6,
        users: 15
    },
    subAccountIds: [4534345, 987893, 876785]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutCorporateSubAccountsPlanRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">inviteAdminUser</a>({ ...params }) -> BrevoApi.InviteAdminUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

`This endpoint allows you to invite a member to manage the Admin account
Features and their respective permissions are as below: - `my_plan`:
  - "all"
- `api`:
  - "none"
- `user_management`:
  - "all"
- `app_management` | Not available in ENTv2:
  - "all"
- `sub_organization_groups`
  - "create"
  - "edit_delete"
- `create_sub_organizations`
  - "all"
- `manage_sub_organizations`
  - "all"
- `analytics`
  - "download_data"
  - "create_alerts"
  - "my_looks"
  - "explore_create"
- `security`
  - "all"
**Note**: - If `all_features_access: false` then only privileges are
required otherwise if `true` then it's assumed that all permissions will be
there for the invited admin user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.inviteAdminUser({
    all_features_access: true,
    email: "inviteuser@example.com",
    privileges: [{}]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.InviteAdminUserRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">resendCancelAdminUserInvitation</a>({ ...params }) -> BrevoApi.PutCorporateUserInvitationActionEmailResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will allow the user to:
- Resend an admin user invitation
- Cancel an admin user invitation
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.resendCancelAdminUserInvitation({
    action: "resend",
    email: "email"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutCorporateUserInvitationActionEmailRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">revokeAnAdminUser</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint allows to revoke/remove an invited member of your Admin
account
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.revokeAnAdminUser({
    email: "email"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteCorporateUserRevokeEmailRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">getCorporateUserPermission</a>({ ...params }) -> BrevoApi.GetCorporateUserPermissionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will provide the list of admin user permissions
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.getCorporateUserPermission({
    email: "email"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCorporateUserPermissionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.masterAccount.<a href="/src/api/resources/masterAccount/client/Client.ts">changeAdminUserPermissions</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will allow you to change the permissions of Admin users of
your Admin account
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.masterAccount.changeAdminUserPermissions({
    email: "email",
    all_features_access: false,
    privileges: [{
            feature: "user_management",
            permissions: ["all"]
        }, {
            feature: "api",
            permissions: ["all"]
        }, {
            feature: "my_plan",
            permissions: ["none"]
        }, {
            feature: "apps_management",
            permissions: ["all"]
        }, {
            feature: "create_sub_organizations",
            permissions: ["all"]
        }, {
            feature: "sub_organization_groups",
            permissions: ["create", "edit_delete"]
        }, {
            feature: "manage_sub_organizations",
            permissions: ["all"]
        }, {
            feature: "security",
            permissions: ["none"]
        }, {
            feature: "analytics",
            permissions: ["create_alerts", "download_data", "my_looks", "explore_create"]
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutCorporateUserEmailPermissionsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MasterAccountClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## User
<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getInvitedUsersList</a>() -> BrevoApi.GetInvitedUsersListResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getInvitedUsersList();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">putRevokeUserPermission</a>({ ...params }) -> BrevoApi.PutRevokeUserPermissionResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.putRevokeUserPermission({
    email: "email"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutRevokeUserPermissionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">inviteuser</a>({ ...params }) -> BrevoApi.InviteuserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

`Feature` - A Feature represents a specific functionality like Email
campaign, Deals, Calls, Automations, etc. on Brevo. While inviting a user,
determine which feature you want to manage access to. You must specify the
feature accurately to avoid errors. `Permission` - A Permission defines the
level of access or control a user has over a specific feature. While
inviting user, decide on the permission level required for the selected
feature. Make sure the chosen permission is related to the selected feature.
Features and their respective permissions are as below: - `email_campaigns`:
  - "create_edit_delete"
  - "send_schedule_suspend"
- `sms_campaigns`:
  - "create_edit_delete"
  - "send_schedule_suspend"
- `contacts`:
  - "view"
  - "create_edit_delete"
  - "import"
  - "export"
  - "list_and_attributes"
  - "forms"
- `templates`:
  - "create_edit_delete"
  - "activate_deactivate"
- `workflows`:
  - "create_edit_delete"
  - "activate_deactivate_pause"
  - "settings"
- `landing_pages`:
  - "all"
- `transactional_emails`:
  - "settings"
  - "logs"
- `smtp_api`:
  - "smtp"
  - "api_keys"
  - "authorized_ips"
- `user_management`:
  - "all"
- `sales_platform`:
  - "create_edit_deals"
  - "delete_deals"
  - "manage_others_deals_tasks"
  - "reports"
  - "settings"
- `phone`:
  - "all"
- `conversations`:
  - "access"
  - "assign"
  - "configure"
- `senders_domains_dedicated_ips`:
  - "senders_management"
  - "domains_management"
  - "dedicated_ips_management"
- `push_notifications`:
  - "view"
  - "create_edit_delete"
  - "send"
  - "settings"
- `companies`:
  - "manage_owned_companies"
  - "manage_other_companies"
  - "settings"
**Note**: - If `all_features_access: false` then only privileges are
required otherwise if `true` then it's assumed that all permissions will be
there for the invited user. - The availability of feature and its permission
depends on your current plan. Please select the features and permissions
accordingly.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.inviteuser({
    all_features_access: true,
    email: "inviteuser@example.com",
    privileges: [{}]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.Inviteuser` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">putresendcancelinvitation</a>({ ...params }) -> BrevoApi.PutresendcancelinvitationResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.putresendcancelinvitation({
    action: "resend",
    email: "email"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutresendcancelinvitationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">editUserPermission</a>({ ...params }) -> BrevoApi.EditUserPermissionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

`Feature` - A Feature represents a specific functionality like Email
campaign, Deals, Calls, Automations, etc. on Brevo. While inviting a user,
determine which feature you want to manage access to. You must specify the
feature accurately to avoid errors. `Permission` - A Permission defines the
level of access or control a user has over a specific feature. While
inviting user, decide on the permission level required for the selected
feature. Make sure the chosen permission is related to the selected feature.
Features and their respective permissions are as below: - `email_campaigns`:
  - "create_edit_delete"
  - "send_schedule_suspend"
- `sms_campaigns`:
  - "create_edit_delete"
  - "send_schedule_suspend"
- `contacts`:
  - "view"
  - "create_edit_delete"
  - "import"
  - "export"
  - "list_and_attributes"
  - "forms"
- `templates`:
  - "create_edit_delete"
  - "activate_deactivate"
- `workflows`:
  - "create_edit_delete"
  - "activate_deactivate_pause"
  - "settings"
- `landing_pages`:
  - "all"
- `transactional_emails`:
  - "settings"
  - "logs"
- `smtp_api`:
  - "smtp"
  - "api_keys"
  - "authorized_ips"
- `user_management`:
  - "all"
- `sales_platform`:
  - "create_edit_deals"
  - "delete_deals"
  - "manage_others_deals_tasks"
  - "reports"
  - "settings"
- `phone`:
  - "all"
- `conversations`:
  - "access"
  - "assign"
  - "configure"
- `senders_domains_dedicated_ips`:
  - "senders_management"
  - "domains_management"
  - "dedicated_ips_management"
- `push_notifications`:
  - "view"
  - "create_edit_delete"
  - "send"
  - "settings"
- `companies`:
  - "manage_owned_companies"
  - "manage_other_companies"
  - "settings"
**Note**: - The privileges array remains the same as in the send invitation;
the user simply needs to provide the permissions that need to be updated. -
The availability of feature and its permission depends on your current plan.
Please select the features and permissions accordingly.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.editUserPermission({
    all_features_access: true,
    email: "inviteuser@example.com",
    privileges: [{}]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.Inviteuser` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.user.<a href="/src/api/resources/user/client/Client.ts">getUserPermission</a>({ ...params }) -> BrevoApi.GetUserPermissionResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.user.getUserPermission({
    email: "email"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetUserPermissionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `UserClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Process
<details><summary><code>client.process.<a href="/src/api/resources/process/client/Client.ts">getProcesses</a>({ ...params }) -> BrevoApi.GetProcessesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves a list of background processes from your Brevo account with filtering and pagination.

**Use this to:**
- Monitor background process activity and status
- Track long-running operations and tasks
- Find process IDs for detailed status checking
- Review process history and performance
- Identify failed or stuck processes for troubleshooting

**Key information returned:**
- Process details (ID, name, type, status)
- Process creation and completion timestamps
- Process progress and completion status
- Error information for failed processes
- Process result data and download links

**Important considerations:**
- Background processes handle long-running operations like imports and exports
- Process status indicates current state (queued, processing, completed, failed, cancelled)
- Export processes provide download URLs when completed
- Failed processes include error messages for troubleshooting
- Use pagination for accounts with many historical processes
- Sort options available for creation order (ascending or descending)
- Different process types handle specific operations (imports, exports, calculations)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.process.getProcesses();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetProcessesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProcessClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.process.<a href="/src/api/resources/process/client/Client.ts">getProcess</a>({ ...params }) -> BrevoApi.GetProcessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves detailed information about a specific background process.

**Use this to:**
- Get detailed status of a specific process
- Monitor process progress and completion
- Download results from completed export processes
- Check error details for failed processes
- Track process execution times

**Key information returned:**
- Complete process details and status
- Import/export statistics and results
- Error information for troubleshooting
- Download URLs for export processes
- Process timing and performance data

**Important considerations:**
- Process ID must exist in your account
- Completed processes provide detailed statistics and results
- Export processes include download URLs when successful
- Failed processes contain error messages for debugging
- Timing information helps with performance analysis
- Different process types return different result structures
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.process.getProcess({
    processId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetProcessRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProcessClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Senders
<details><summary><code>client.senders.<a href="/src/api/resources/senders/client/Client.ts">getSenders</a>({ ...params }) -> BrevoApi.GetSendersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves a list of all email senders from your Brevo account with optional filtering.

**Use this to:**
- Get all available senders for email campaign setup
- Find sender details including ID, name, and email address
- Filter senders by IP address for dedicated IP users
- Filter senders by domain for domain-specific configurations
- Monitor sender configuration and status

**Key information returned:**
- Sender details (ID, name, email address)
- Sender status and verification information
- Associated IP addresses and domains (for dedicated IP accounts)
- Sender configuration settings

**Important considerations:**
- Standard accounts show empty IP arrays, dedicated IP accounts show IP assignments
- Filtering by IP only available for accounts with dedicated IPs
- Domain filtering helps organize senders by business units or brands
- Sender status indicates if sender is active and ready for campaign use
- Email verification required before sender can be used in campaigns
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.senders.getSenders();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetSendersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SendersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.senders.<a href="/src/api/resources/senders/client/Client.ts">createSender</a>({ ...params }) -> BrevoApi.CreateSenderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new email sender in your Brevo account.

**Use this to:**
- Add new senders for email campaigns
- Configure sender identity (name and email)
- Associate dedicated IPs with the sender (for dedicated IP accounts)
- Set up domain-based sender configurations

**Key information returned:**
- Created sender ID
- DKIM and SPF configuration status
- Success confirmation

**Important considerations:**
- Verification email sent to specified sender address
- DKIM and SPF configuration affects deliverability
- Dedicated IP accounts require IP association during creation
- IP weights must sum to 100 when specified
- Sender must be verified before use in campaigns
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.senders.createSender({
    email: "support@example.com",
    name: "Support Team"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateSenderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SendersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.senders.<a href="/src/api/resources/senders/client/Client.ts">getIps</a>() -> BrevoApi.GetIpsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves all dedicated IPs associated with your Brevo account.

Use this to:
- List all your dedicated IPs
- Check the status of your dedicated IPs (active/inactive)
- Find IP addresses and associated domains for configuration purposes
- Monitor your IP reputation and deliverability
- Verify available IPs for sender configuration

Key information returned:
- IP ID and address
- Associated domain
- Active status
- IP configuration details
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.senders.getIps();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `SendersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.senders.<a href="/src/api/resources/senders/client/Client.ts">updateSender</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing email sender's configuration.

Use this to:
- Modify sender display name or email address
- Update dedicated IP associations
- Change sender configuration settings
- Correct sender information

Key information returned:
- Success confirmation
- Updated sender details
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.senders.updateSender({
    senderId: 1000000,
    name: "New Support Team"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateSenderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SendersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.senders.<a href="/src/api/resources/senders/client/Client.ts">deleteSender</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes an email sender from your Brevo account.

Use this to:
- Remove senders that are no longer needed
- Clean up sender configurations
- Remove duplicate or test senders

Key information returned:
- Success confirmation message
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.senders.deleteSender({
    senderId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteSenderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SendersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.senders.<a href="/src/api/resources/senders/client/Client.ts">getIpsFromSender</a>({ ...params }) -> BrevoApi.GetIpsFromSenderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves the dedicated IPs associated with a specific sender.

Use this to:
- Check IP configuration for a sender
- Verify dedicated IP associations
- Get IP details for troubleshooting
- Monitor sender IP configuration

Key information returned:
- List of associated dedicated IPs
- IP addresses and domain configurations
- IP status and settings
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.senders.getIpsFromSender({
    senderId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetIpsFromSenderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SendersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.senders.<a href="/src/api/resources/senders/client/Client.ts">validateSenderByOtp</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Validates a sender using the OTP (One-Time Password) received via email.

Use this to:
- Complete sender verification process
- Activate a newly created sender
- Verify ownership of the sender email address
- Enable the sender for use in email campaigns

Key information returned:
- Success confirmation of sender verification
- Sender activation status
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.senders.validateSenderByOtp({
    senderId: 1000000,
    otp: 123456
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.ValidateSenderByOtpRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SendersClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Domains
<details><summary><code>client.domains.<a href="/src/api/resources/domains/client/Client.ts">getDomains</a>() -> BrevoApi.GetDomainsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves all domains associated with the account.

Use this to:
- List all domains
- Verify domain existence
- Check domain authentication and verification status
- Monitor domain configuration and provider information
- Review domain creation history and ownership

Key information returned:
- Domain details (ID, name, authentication status)
- Verification and authentication states
- Associated IP addresses and DNS providers
- Creator information and creation timestamps
- Pagination information for large domain lists
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.domains.getDomains();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `DomainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.domains.<a href="/src/api/resources/domains/client/Client.ts">createDomain</a>({ ...params }) -> BrevoApi.CreateDomainResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new domain in Brevo.

Use this to:
- Add new domains for sending emails
- Set up domain authentication for better deliverability
- Configure DNS records for email authentication
- Establish domain-based sender identities

Key information returned:
- Created domain ID and configuration
- Required DNS records for authentication
- Domain provider detection results
- Setup instructions and next steps
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.domains.createDomain({
    name: "mycompany.com"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateDomainRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DomainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.domains.<a href="/src/api/resources/domains/client/Client.ts">getDomainConfiguration</a>({ ...params }) -> BrevoApi.GetDomainConfigurationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves configuration of a specific domain, to know if the domain is valid or not.

Use this to:
- Check domain configuration
- Validate a domain configuration
- Monitor DNS record status
- Troubleshoot authentication issues

Key information returned:
- Domain verification and authentication status
- DNS records configuration and validation status
- Detailed authentication requirements
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.domains.getDomainConfiguration({
    domainName: "domainName"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetDomainConfigurationRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DomainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.domains.<a href="/src/api/resources/domains/client/Client.ts">deleteDomain</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes a domain from Brevo.

Use this to:
- Remove existing domains
- Clean up unused domain configurations
- Remove test domains

Key information returned:
- Success confirmation message
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.domains.deleteDomain({
    domainName: "domainName"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteDomainRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DomainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.domains.<a href="/src/api/resources/domains/client/Client.ts">authenticateDomain</a>({ ...params }) -> BrevoApi.AuthenticateDomainResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Authenticates a specific domain.

Use this to:
- Authenticate a domain
- Verify DNS record configuration
- Complete domain setup for sending
- Enable domain for email authentication

Key information returned:
- Authentication success confirmation
- Domain readiness status for email sending
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.domains.authenticateDomain({
    domainName: "domainName"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.AuthenticateDomainRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DomainsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Webhooks
<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">getWebhooks</a>({ ...params }) -> BrevoApi.GetWebhooksResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves all webhooks from your Brevo account with filtering and sorting options.

Use this to:
- Monitor webhook configurations and event handling
- List webhooks by type (transactional, marketing, inbound)
- Review webhook endpoints and authentication
- Track webhook creation and modification history
- Audit webhook event subscriptions

Key information returned:
- Complete webhook details and configuration
- Event types and channel subscriptions
- Authentication and security settings
- Webhook URLs and custom headers
- Creation and modification timestamps
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.getWebhooks();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetWebhooksRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">createWebhook</a>({ ...params }) -> BrevoApi.CreateWebhookResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new webhook to receive real-time notifications for specified events.

Use this to:
- Set up event notifications for transactional or marketing emails
- Configure webhook endpoints for campaign tracking
- Enable real-time monitoring of email delivery status
- Subscribe to contact list changes and updates
- Implement custom event handling and automation

Key information returned:
- Created webhook ID and configuration
- Success confirmation and setup details
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.createWebhook({
    events: ["sent"],
    url: "http://requestb.in/173lyyx1"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateWebhookRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">exportWebhooksHistory</a>({ ...params }) -> BrevoApi.ExportWebhooksHistoryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note title="This feature is available for Professional and Enterprise plans">
To have it activated please send us a request and we will activate it for your account.
</Note>

Exports webhook event history to CSV format for analysis and reporting.

Use this to:
- Generate comprehensive webhook event reports
- Analyze webhook delivery patterns and success rates
- Export event data for external analysis tools
- Create historical reports for compliance and auditing
- Track webhook performance and reliability metrics

Key information returned:
- Process ID for tracking export completion
- CSV file will be delivered to specified webhook URL
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.exportWebhooksHistory({
    event: "invalid_parameter",
    notifyURL: "https://brevo.com",
    type: "transactional"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.ExportWebhooksHistoryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">getWebhook</a>({ ...params }) -> BrevoApi.GetWebhook</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves detailed information about a specific webhook configuration.

Use this to:
- Get complete webhook configuration and settings
- Check webhook event subscriptions and triggers
- Review authentication and security settings
- Verify webhook URL and custom headers
- Access webhook creation and modification history

Key information returned:
- Complete webhook details and configuration
- Event types and channel subscriptions
- Authentication credentials and methods
- Custom headers and request settings
- Webhook status and activity information
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.getWebhook({
    webhookId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetWebhookRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">updateWebhook</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing webhook configuration and event subscriptions.

Use this to:
- Modify webhook event subscriptions and triggers
- Update webhook URL and endpoint configuration
- Change authentication settings and credentials
- Adjust custom headers and request parameters
- Enable or disable specific webhook events

Key information returned:
- Success confirmation of webhook updates
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.updateWebhook({
    webhookId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateWebhookRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.<a href="/src/api/resources/webhooks/client/Client.ts">deleteWebhook</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently deletes a webhook and stops all event notifications.

Use this to:
- Remove unused or obsolete webhook configurations
- Clean up webhook endpoints and subscriptions
- Stop event notifications to specific URLs
- Maintain organized webhook management

Key information returned:
- Success confirmation of webhook deletion
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.webhooks.deleteWebhook({
    webhookId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteWebhookRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## ExternalFeeds
<details><summary><code>client.externalFeeds.<a href="/src/api/resources/externalFeeds/client/Client.ts">getAllExternalFeeds</a>({ ...params }) -> BrevoApi.GetAllExternalFeedsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves all external feeds from your Brevo account with filtering and pagination.

**Use this to:**
- Get an overview of all external data feeds
- Find feeds by name using search functionality
- Filter feeds by creation date range
- Browse feeds by authentication type
- Monitor feed library organization and usage

**Key information returned:**
- Feed details (UUID, name, URL, authentication type)
- Feed configuration and settings
- Creation and modification timestamps
- Feed status and error information
- Authentication and header configurations

**Important considerations:**
- External feeds enable dynamic content in email campaigns
- Feeds must be accessible from Brevo servers
- Authentication credentials are securely stored
- Feed performance affects campaign delivery
- Use pagination for accounts with many feeds
- Date range filtering limited to 30 days maximum
- Search functionality works on feed name matching
- Internal feeds are system-managed and cannot be modified
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.externalFeeds.getAllExternalFeeds({
    search: "product",
    startDate: "2024-01-01",
    endDate: "2024-01-31"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetAllExternalFeedsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ExternalFeedsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.externalFeeds.<a href="/src/api/resources/externalFeeds/client/Client.ts">createExternalFeed</a>({ ...params }) -> BrevoApi.CreateExternalFeedResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new external feed for dynamic content in email campaigns.

**Use this to:**
- Set up external data sources for dynamic content
- Configure authentication for protected feeds
- Enable real-time content updates in campaigns
- Establish connections to product catalogs, blogs, or APIs

**Key information returned:**
- Created feed UUID for reference in campaigns
- Success confirmation

**Important considerations:**
- Feed URL must be accessible from Brevo infrastructure
- Authentication credentials are securely encrypted
- Test feed accessibility before campaign use
- Consider feed response time for campaign performance
- Monitor feed reliability and uptime
- Use caching for frequently accessed feeds
- Maximum 5 retry attempts allowed for failed requests
- Custom headers support for API integration requirements
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.externalFeeds.createExternalFeed({
    name: "Public API Feed",
    url: "https://jsonplaceholder.typicode.com/posts",
    authType: "noAuth",
    maxRetries: 3,
    cache: true
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateExternalFeedRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ExternalFeedsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.externalFeeds.<a href="/src/api/resources/externalFeeds/client/Client.ts">getExternalFeedByUuid</a>({ ...params }) -> BrevoApi.GetExternalFeedByUuidResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieves details of a specific external feed by its UUID.

**Use this to:**
- Get complete configuration of an external feed
- Check feed authentication settings
- Review feed personalization options
- Verify feed URL and parameters
- Monitor feed modification history

**Key information returned:**
- Complete feed configuration and settings
- Authentication credentials and headers
- Personalization and fallback settings
- Creation and modification timestamps
- Cache and retry configurations

**Important considerations:**
- UUID must exist in your account
- Provides complete feed information for troubleshooting
- Essential before making modifications
- Shows current feed health status
- Useful for debugging feed issues
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.externalFeeds.getExternalFeedByUuid({
    uuid: "b1c2d3e4-f5a6-47b8-89c0-d1e2f3a4b5c6"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetExternalFeedByUuidRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ExternalFeedsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.externalFeeds.<a href="/src/api/resources/externalFeeds/client/Client.ts">updateExternalFeed</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates configuration of an existing external feed.

**Use this to:**
- Update feed URLs when data sources change
- Modify authentication credentials
- Change cache and retry settings
- Update custom headers
- Rename feeds for better organization

**Key information returned:**
- Success confirmation message

**Important considerations:**
- Only provided fields will be updated
- Feed UUID must exist in your account
- Authentication changes require verification
- URL changes should be tested before campaign use
- Monitor campaigns using this feed after updates
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.externalFeeds.updateExternalFeed({
    uuid: "b1c2d3e4-f5a6-47b8-89c0-d1e2f3a4b5c6",
    name: "Updated Product Catalog",
    url: "https://api.newstore.com/products/v2"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateExternalFeedRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ExternalFeedsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.externalFeeds.<a href="/src/api/resources/externalFeeds/client/Client.ts">deleteExternalFeed</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes an external feed from your Brevo account.

**Use this to:**
- Remove external feeds that are no longer needed
- Clean up unused data sources
- Remove test or outdated feeds
- Maintain organized feed library

**Key information returned:**
- Success confirmation message

**Important considerations:**
- This action is PERMANENT and cannot be undone
- Feed configuration and history will be lost
- Check if feed is used in active campaigns before deletion
- Remove feed references from email templates
- Consider deactivating instead of deleting if unsure
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.externalFeeds.deleteExternalFeed({
    uuid: "b1c2d3e4-f5a6-47b8-89c0-d1e2f3a4b5c6"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteExternalFeedRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ExternalFeedsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## CustomObjects
<details><summary><code>client.customObjects.<a href="/src/api/resources/customObjects/client/Client.ts">upsertrecords</a>({ ...params }) -> BrevoApi.UpsertrecordsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note title="Enterprise access only">
Custom objects are only available to Enterprise plans.

This feature is in beta. These are subject to change.
</Note>

This API allows bulk upsert of object records in a single request. Each object record may include
  - Attributes
  - Identifiers
  - Associations
**Response:**
  The API processes the request asynchronously and returns a processId that you can use to track the background process status.
**API and Schema Limitation:**
  - Size:
      - Max 1000 objects records per request
      - Max request body size: 1 MB
  - Max 500 attributes defined per object record upsert request
    - This is coherent with schema limitation: an object cannot have more than 500 attributes.
    - Worth noting: Nothing happens If an attribute is mentioned in the request, but was not previously defined for the object schema (no error, no attribute creation)
  - Max 10 associations defined per object record upsert request
    - This is coherent with schema limitation: an object cannot have more than 10 associations with other objects. and each object record can be linked to max 10 other records.
**Errors:**
    - Make sure both object records exist before associating them, else the API will return an error.
    - This route does not create objects. The object where the object records are upserted by this API must be created already else the API will return an error "invalid object type".
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customObjects.upsertrecords({
    object_type: "vehicle",
    records: [{}]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpsertrecordsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomObjectsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customObjects.<a href="/src/api/resources/customObjects/client/Client.ts">getrecords</a>({ ...params }) -> BrevoApi.GetrecordsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note title="Enterprise access only">
Custom objects are only available to Enterprise plans.

This feature is in beta. These are subject to change.
</Note>

This API retrieves a list of object records along with their associated records and provides the total count of records for the specified object. **Note**: Contact as object type is not supported in this endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customObjects.getrecords({
    object_type: "vehicle",
    limit: 1000000,
    page_num: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetrecordsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomObjectsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.customObjects.<a href="/src/api/resources/customObjects/client/Client.ts">batchDeleteObjectRecords</a>({ ...params }) -> BrevoApi.BatchDeleteObjectRecordsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Use this endpoint to delete multiple object records of the same object-type in one request.
The request is accepted and processed asynchronously.   You can track the status of the deletion process using the returned **processId**.
**API and Schema Limitations:** - Each request can contain up to **1000** object record identifiers   - If more records must be deleted → send multiple batch requests
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.customObjects.batchDeleteObjectRecords({
    object_type: "vehicle",
    identifiers: {
        ext_ids: ["ext-001", "ext-002"]
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.BatchDeleteObjectRecordsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CustomObjectsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Contacts
<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getContacts</a>({ ...params }) -> BrevoApi.GetContacts</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note title="Follow this format when passing a SMS phone number as an attribute">
Accepted Number Formats

91xxxxxxxxxx
+91xxxxxxxxxx
0091xxxxxxxxxx
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getContacts();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">createContact</a>({ ...params }) -> BrevoApi.CreateContactResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates new contacts on Brevo. Contacts can be created by passing either - <br><br> 1. email address of the contact (email_id),  <br> 2. phone number of the contact (to be passed as "SMS" field in "attributes" along with proper country code), For example- {"SMS":"+91xxxxxxxxxx"} or {"SMS":"0091xxxxxxxxxx"} <br> 3. ext_id <br>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.createContact();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getAttributes</a>() -> BrevoApi.GetAttributesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getAttributes();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">createAttribute</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.createAttribute({
    attributeCategory: "normal",
    attributeName: "attributeName"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateAttributeRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">updateAttribute</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.updateAttribute({
    attributeCategory: "category",
    attributeName: "attributeName"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateAttributeRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">deleteAttribute</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.deleteAttribute({
    attributeCategory: "normal",
    attributeName: "attributeName"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteAttributeRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">deleteMultiAttributeOptions</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.deleteMultiAttributeOptions({
    attributeType: "multiple-choice",
    multipleChoiceAttribute: "multipleChoiceAttribute",
    multipleChoiceAttributeOption: "multipleChoiceAttributeOption"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteMultiAttributeOptionsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">updateBatchContacts</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.updateBatchContacts();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateBatchContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">createDoiContact</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note title="How to use attributes param?">
attributes param in this endpoint is an object containing key-value pairs where values can be either a string, integer, array, or boolean. You can create key-value pairs with these four datatypes. When a value is an array, it should be an array of strings.
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.createDoiContact({
    email: "elly@example.com",
    includeListIds: [36],
    redirectionUrl: "http://requestb.in/173lyyx1",
    templateId: 2
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateDoiContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">requestContactExport</a>({ ...params }) -> BrevoApi.RequestContactExportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

It returns the background process ID which on completion calls the notify URL that you have set in the input. File will be available in csv.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.requestContactExport({
    customContactFilter: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.RequestContactExportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getFolders</a>({ ...params }) -> BrevoApi.GetFoldersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
Ongoing changes for this endpoint

We're dropping support for the response attributes totalSubscribers and totalBlacklisted.

These are non breaking changes.

The default value for the attributes will be 0.

The uniqueSubscribers field is deprecated
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getFolders();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetFoldersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">createFolder</a>({ ...params }) -> BrevoApi.CreateFolderResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.createFolder({});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateUpdateFolder` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getFolder</a>({ ...params }) -> BrevoApi.GetFolder</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
Ongoing changes for this endpoint.

We're dropping support for the response attributes totalSubscribers and totalBlacklisted.

These are non breaking changes. The default value for the attributes will be 0.
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getFolder({
    folderId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetFolderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">updateFolder</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.updateFolder({
    folderId: 1000000,
    body: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateFolderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">deleteFolder</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.deleteFolder({
    folderId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteFolderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getFolderLists</a>({ ...params }) -> BrevoApi.GetFolderListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
Ongoing changes for this endpoint.

We're dropping support for the response attributes totalSubscribers and totalBlacklisted.

These are non breaking changes. The default value for the attributes will be 0.
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getFolderLists({
    folderId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetFolderListsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">importContacts</a>({ ...params }) -> BrevoApi.ImportContactsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

It returns the background process ID which on completion calls the notify URL that you have set in the input. **Note**: - Any contact attribute that doesn't exist in your account will be ignored at import end.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.importContacts();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.ImportContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getLists</a>({ ...params }) -> BrevoApi.GetListsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
Ongoing changes for this endpoint.

We're dropping support for the response attributes totalSubscribers and totalBlacklisted.

These are non breaking changes. The default value for the attributes will be 0.
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getLists();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetListsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">createList</a>({ ...params }) -> BrevoApi.CreateListResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.createList({
    folderId: 2,
    name: "Magento Customer - ES"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getList</a>({ ...params }) -> BrevoApi.GetListResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getList({
    listId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">updateList</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.updateList({
    listId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">deleteList</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.deleteList({
    listId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getContactsFromList</a>({ ...params }) -> BrevoApi.GetContacts</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getContactsFromList({
    listId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetContactsFromListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">addContactToList</a>({ ...params }) -> BrevoApi.PostContactInfo</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.addContactToList({
    listId: 1000000,
    body: {
        emails: ["jeff32@example.com", "jim56@example.com"]
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.AddContactToListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">removeContactFromList</a>({ ...params }) -> BrevoApi.PostContactInfo</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.removeContactFromList({
    listId: 1000000,
    body: {
        all: true
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.RemoveContactFromListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getSegments</a>({ ...params }) -> BrevoApi.GetSegmentsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getSegments();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetSegmentsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getContactInfo</a>({ ...params }) -> BrevoApi.GetContactInfoResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note title="Follow this format when passing a SMS phone number as an attribute">
Accepted Number Formats

91xxxxxxxxxx
+91xxxxxxxxxx
0091xxxxxxxxxx
</Note>

There are 2 ways to get a contact <br><br> Option 1- https://api.brevo.com/v3/contacts/{identifier} <br><br> Option 2- https://api.brevo.com/v3/contacts/{identifier}?identifierType={} <br> <br> Option 1 only works if identifierType is email_id (for EMAIL), phone_id (for SMS) or contact_id (for ID of the contact),where you can directly pass the value of EMAIL, SMS and ID of the contact.   <br><br> Option 2 works for all identifierType, use email_id for EMAIL attribute, phone_id for SMS attribute, contact_id for ID of the contact, ext_id for EXT_ID attribute, whatsapp_id for WHATSAPP attribute, landline_number_id for LANDLINE_NUMBER attribute <br><br>Along with the contact details, this endpoint will show the statistics of contact for the recent 90 days by default. To fetch the earlier statistics, please use Get contact campaign stats ``https://developers.brevo.com/reference/contacts-7#getcontactstats`` endpoint with the appropriate date ranges.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getContactInfo({
    identifier: "identifier"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetContactInfoRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">updateContact</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

There are 2 ways to update a contact <br><br> Option 1- https://api.brevo.com/v3/contacts/{identifier} <br><br> Option 2- https://api.brevo.com/v3/contacts/{identifier}?identifierType={} <br> <br> Option 1 only works if identifierType is email_id (for EMAIL) or contact_id (for ID of the contact),where you can directly pass the value of EMAIL and ID of the contact.   <br><br> Option 2 works for all identifierType, use email_id for EMAIL attribute, contact_id for ID of the contact, ext_id for EXT_ID attribute, phone_id for SMS attribute, whatsapp_id for WHATSAPP attribute, landline_number_id for LANDLINE attribute
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.updateContact({
    identifier: "identifier"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">deleteContact</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

There are 2 ways to delete a contact <br><br> Option 1- https://api.brevo.com/v3/contacts/{identifier} <br><br> Option 2- https://api.brevo.com/v3/contacts/{identifier}?identifierType={} <br> <br> Option 1 only works if identifierType is email_id (for EMAIL) or contact_id (for ID of the contact),where you can directly pass the value of EMAIL and ID of the contact.   <br><br> Option 2 works for all identifierType, use email_id for EMAIL attribute, contact_id for ID of the contact, ext_id for EXT_ID attribute, phone_id for SMS attribute, whatsapp_id for WHATSAPP attribute, landline_number_id for LANDLINE_NUMBER attribute.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.deleteContact({
    identifier: "identifier"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteContactRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contacts.<a href="/src/api/resources/contacts/client/Client.ts">getContactStats</a>({ ...params }) -> BrevoApi.GetContactStatsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.contacts.getContactStats({
    identifier: "identifier"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetContactStatsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ContactsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Conversations
<details><summary><code>client.conversations.<a href="/src/api/resources/conversations/client/Client.ts">setsAgentsStatusToOnlineFor23Minutes</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

We recommend pinging this endpoint every minute for as long as the agent has to be considered online.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.conversations.setsAgentsStatusToOnlineFor23Minutes({
    agentId: "d9nKoegKSjmCtyK78"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostConversationsAgentOnlinePingRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="/src/api/resources/conversations/client/Client.ts">sendAMessageAsAnAgent</a>({ ...params }) -> BrevoApi.ConversationsMessage</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.conversations.sendAMessageAsAnAgent({
    agentId: "d9nKoegKSjmCtyK78",
    text: "Hello! How can I help you?",
    visitorId: "kZMvWhf8npAu3H6qd57w2Hv6nh6rnxvg"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostConversationsMessagesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="/src/api/resources/conversations/client/Client.ts">getAMessage</a>({ ...params }) -> BrevoApi.ConversationsMessage</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.conversations.getAMessage({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetConversationsMessagesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="/src/api/resources/conversations/client/Client.ts">updateAMessageSentByAnAgent</a>({ ...params }) -> BrevoApi.ConversationsMessage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Only agents’ messages can be edited.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.conversations.updateAMessageSentByAnAgent({
    id: "id",
    text: "Good morning! How can I help you?"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutConversationsMessagesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="/src/api/resources/conversations/client/Client.ts">deleteAMessageSentByAnAgent</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Only agents’ messages can be deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.conversations.deleteAMessageSentByAnAgent({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteConversationsMessagesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="/src/api/resources/conversations/client/Client.ts">sendAnAutomatedMessageToAVisitor</a>({ ...params }) -> BrevoApi.ConversationsMessage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Example of automated messages: order status, announce new features in your web app, etc.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.conversations.sendAnAutomatedMessageToAVisitor({
    groupId: "PjRBMhWGen6aRHjif",
    text: "Your order has shipped! Here\u2019s your tracking number: 9114 5847 3325 9667 4328 88",
    visitorId: "kZMvWhf8npAu3H6qd57w2Hv6nh6rnxvg"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostConversationsPushedMessagesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="/src/api/resources/conversations/client/Client.ts">getAnAutomatedMessage</a>({ ...params }) -> BrevoApi.ConversationsMessage</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.conversations.getAnAutomatedMessage({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetConversationsPushedMessagesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="/src/api/resources/conversations/client/Client.ts">updateAnAutomatedMessage</a>({ ...params }) -> BrevoApi.ConversationsMessage</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.conversations.updateAnAutomatedMessage({
    id: "id",
    text: "Your order has shipped! Here\u2019s your tracking number: 9114 5847 4668 7775 9233 54"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutConversationsPushedMessagesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="/src/api/resources/conversations/client/Client.ts">deleteAnAutomatedMessage</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.conversations.deleteAnAutomatedMessage({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteConversationsPushedMessagesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.conversations.<a href="/src/api/resources/conversations/client/Client.ts">setVisitorGroupAssignment</a>({ ...params }) -> BrevoApi.PutConversationsVisitorGroupResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Assigns a visitor to a specific agent group or removes them from their current group.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.conversations.setVisitorGroupAssignment({
    groupId: "PjRBMhWGen6aRHjif"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PutConversationsVisitorGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ConversationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Ecommerce
<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">getCategories</a>({ ...params }) -> BrevoApi.GetCategoriesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.getCategories();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCategoriesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">createUpdateCategory</a>({ ...params }) -> BrevoApi.CreateUpdateCategoryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.createUpdateCategory({
    id: "CAT123"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateUpdateCategoryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">createUpdateBatchCategory</a>({ ...params }) -> BrevoApi.CreateUpdateBatchCategoryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.createUpdateBatchCategory({
    categories: [{
            id: "CAT123"
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateUpdateBatchCategoryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">getCategoryInfo</a>({ ...params }) -> BrevoApi.GetCategoryDetails</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.getCategoryInfo({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCategoryInfoRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">activateTheECommerceApp</a>() -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Getting access to Brevo eCommerce.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.activateTheECommerceApp();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">getAttributionMetricsForOneOrMoreBrevoCampaignsOrWorkflows</a>({ ...params }) -> BrevoApi.GetEcommerceAttributionMetricsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.getAttributionMetricsForOneOrMoreBrevoCampaignsOrWorkflows({
    periodFrom: "2022-01-02T00:00:00Z",
    periodTo: "2022-01-03T00:00:00Z"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetEcommerceAttributionMetricsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">getDetailedAttributionMetricsForASingleBrevoCampaignOrWorkflow</a>({ ...params }) -> BrevoApi.GetEcommerceAttributionMetricsConversionSourceConversionSourceIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.getDetailedAttributionMetricsForASingleBrevoCampaignOrWorkflow({
    conversionSource: "email_campaign",
    conversionSourceId: "sale"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetEcommerceAttributionMetricsConversionSourceConversionSourceIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">getAttributedProductSalesForASingleBrevoCampaignOrWorkflow</a>({ ...params }) -> BrevoApi.GetEcommerceAttributionProductsConversionSourceConversionSourceIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.getAttributedProductSalesForASingleBrevoCampaignOrWorkflow({
    conversionSource: "email_campaign",
    conversionSourceId: "sale"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetEcommerceAttributionProductsConversionSourceConversionSourceIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">getTheIso4217CompliantDisplayCurrencyCodeForYourBrevoAccount</a>() -> BrevoApi.GetEcommerceConfigDisplayCurrencyResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.getTheIso4217CompliantDisplayCurrencyCodeForYourBrevoAccount();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">setConfigDisplayCurrency</a>({ ...params }) -> BrevoApi.SetConfigDisplayCurrencyResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.setConfigDisplayCurrency({
    code: "EUR"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SetConfigDisplayCurrencyRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">getOrders</a>({ ...params }) -> unknown</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get all the orders
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.getOrders();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">createOrder</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Manages the transactional status of the order
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.createOrder({
    amount: 308.42,
    createdAt: "2021-07-29T20:59:23.383Z",
    id: "14",
    products: [{
            price: 99.99,
            productId: "P1",
            quantity: 10
        }],
    status: "completed",
    updatedAt: "2021-07-30T10:59:23.383Z"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.Order` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">createBatchOrder</a>({ ...params }) -> BrevoApi.CreateBatchOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create multiple orders at one time instead of one order at a time
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.createBatchOrder({
    orders: [{
            amount: 308.42,
            createdAt: "2021-07-29T20:59:23.383Z",
            id: "14",
            products: [{
                    price: 99.99,
                    productId: "P1",
                    quantity: 10
                }],
            status: "completed",
            updatedAt: "2021-07-30T10:59:23.383Z"
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateBatchOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">getProducts</a>({ ...params }) -> BrevoApi.GetProductsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.getProducts();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetProductsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">createUpdateProduct</a>({ ...params }) -> BrevoApi.CreateUpdateProductResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.createUpdateProduct({
    id: "P11",
    name: "Iphone 11"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateUpdateProductRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">createUpdateBatchProducts</a>({ ...params }) -> BrevoApi.CreateUpdateBatchProductsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.createUpdateBatchProducts({
    products: [{
            id: "P11",
            name: "Iphone 11"
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateUpdateBatchProductsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">getProductInfo</a>({ ...params }) -> BrevoApi.GetProductDetails</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.getProductInfo({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetProductInfoRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ecommerce.<a href="/src/api/resources/ecommerce/client/Client.ts">createProductAlert</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.ecommerce.createProductAlert({
    id: "id",
    type: "back_in_stock"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateProductAlertRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EcommerceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Coupons
<details><summary><code>client.coupons.<a href="/src/api/resources/coupons/client/Client.ts">getCouponCollections</a>({ ...params }) -> BrevoApi.GetCouponCollection</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.coupons.getCouponCollections();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCouponCollectionsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CouponsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.coupons.<a href="/src/api/resources/coupons/client/Client.ts">createCouponCollection</a>({ ...params }) -> BrevoApi.CreateCouponCollectionResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.coupons.createCouponCollection({
    defaultCoupon: "Winter",
    name: "10%OFF"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateCouponCollectionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CouponsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.coupons.<a href="/src/api/resources/coupons/client/Client.ts">getCouponCollection</a>({ ...params }) -> BrevoApi.GetCouponCollection</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.coupons.getCouponCollection({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCouponCollectionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CouponsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.coupons.<a href="/src/api/resources/coupons/client/Client.ts">updateCouponCollection</a>({ ...params }) -> BrevoApi.UpdateCouponCollectionResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.coupons.updateCouponCollection({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateCouponCollectionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CouponsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.coupons.<a href="/src/api/resources/coupons/client/Client.ts">createCoupons</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.coupons.createCoupons({
    collectionId: "23befbae-1505-47a8-bd27-e30ef739f32c",
    coupons: ["Uf12AF"]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateCouponsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CouponsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Payments
<details><summary><code>client.payments.<a href="/src/api/resources/payments/client/Client.ts">createPaymentRequest</a>({ ...params }) -> BrevoApi.CreatePaymentRequestResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payments.createPaymentRequest({
    cart: {
        currency: "EUR",
        specificAmount: 1200
    },
    contactId: 43,
    reference: "Invoice #INV0001"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreatePaymentRequestRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.payments.<a href="/src/api/resources/payments/client/Client.ts">getPaymentRequest</a>({ ...params }) -> BrevoApi.GetPaymentRequestResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payments.getPaymentRequest({
    id: "050db7b0-9bb7-4c1e-9c68-5a8dace8c1dc"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetPaymentRequestRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.payments.<a href="/src/api/resources/payments/client/Client.ts">deletePaymentRequest</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.payments.deletePaymentRequest({
    id: "9ae7d68a-565c-4695-9381-d8fb3e3a14cc"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeletePaymentRequestRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Event
<details><summary><code>client.event.<a href="/src/api/resources/event/client/Client.ts">createEvent</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an event to track a contact's interaction.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.event.createEvent({
    event_name: "video_played",
    identifiers: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateEventRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## InboundParsing
<details><summary><code>client.inboundParsing.<a href="/src/api/resources/inboundParsing/client/Client.ts">getInboundEmailEvents</a>({ ...params }) -> BrevoApi.GetInboundEmailEventsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will show the list of all the events for the received emails.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.inboundParsing.getInboundEmailEvents();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetInboundEmailEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `InboundParsingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.inboundParsing.<a href="/src/api/resources/inboundParsing/client/Client.ts">getInboundEmailEventsByUuid</a>({ ...params }) -> BrevoApi.GetInboundEmailEventsByUuidResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will show the list of all events history for one particular received email.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.inboundParsing.getInboundEmailEventsByUuid({
    uuid: "uuid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetInboundEmailEventsByUuidRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `InboundParsingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.inboundParsing.<a href="/src/api/resources/inboundParsing/client/Client.ts">getInboundEmailAttachment</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will retrieve inbound attachment with download token.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.inboundParsing.getInboundEmailAttachment({
    downloadToken: "downloadToken"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetInboundEmailAttachmentRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `InboundParsingClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Balance
<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">getActiveBalancesApi</a>({ ...params }) -> BrevoApi.BalanceLimit</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns Active Balances
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.getActiveBalancesApi({
    pid: "pid",
    contact_id: 1,
    balance_definition_id: "balance_definition_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetLoyaltyBalanceProgramsPidActiveBalanceRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">getBalanceDefinitionList</a>({ ...params }) -> BrevoApi.GetBalanceDefinitionListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns balance definition page
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.getBalanceDefinitionList({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetBalanceDefinitionListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">createBalanceDefinition</a>({ ...params }) -> BrevoApi.BalanceDefinition</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates balance definition and returns information
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.createBalanceDefinition({
    pid: "pid",
    name: "name",
    unit: "POINTS"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostLoyaltyBalanceProgramsPidBalanceDefinitionsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">getBalanceDefinition</a>({ ...params }) -> BrevoApi.BalanceDefinition</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns balance definition
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.getBalanceDefinition({
    pid: "pid",
    bdid: "bdid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetBalanceDefinitionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">updateBalanceDefinition</a>({ ...params }) -> BrevoApi.BalanceDefinition</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates Balance definition
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.updateBalanceDefinition({
    pid: "pid",
    bdid: "bdid",
    name: "name",
    unit: "POINTS"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateBalanceDefinitionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">deleteBalanceDefinition</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete Balance definition
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.deleteBalanceDefinition({
    pid: "pid",
    bdid: "bdid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteBalanceDefinitionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">createBalanceLimit</a>({ ...params }) -> BrevoApi.BalanceLimit</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates balance limit and sends the created UUID along with the data
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.createBalanceLimit({
    pid: "pid",
    bdid: "bdid",
    constraintType: "transaction",
    durationUnit: "day",
    durationValue: 1,
    transactionType: "credit",
    value: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateBalanceLimitRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">getBalanceLimit</a>({ ...params }) -> BrevoApi.BalanceLimit</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Fetches balance limits and send the created UUID along with the data
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.getBalanceLimit({
    pid: "pid",
    bdid: "bdid",
    blid: "blid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetBalanceLimitRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">updateBalanceLimit</a>({ ...params }) -> BrevoApi.BalanceLimit</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates balance limit
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.updateBalanceLimit({
    pid: "pid",
    bdid: "bdid",
    blid: "blid",
    constraintType: "transaction",
    durationUnit: "day",
    durationValue: 1,
    transactionType: "credit",
    value: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateBalanceLimitRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">deleteBalanceLimit</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete balance limit
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.deleteBalanceLimit({
    pid: "pid",
    bdid: "bdid",
    blid: "blid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteBalanceLimitRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">getContactBalances</a>({ ...params }) -> BrevoApi.GetContactBalancesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns balance list
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.getContactBalances({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetContactBalancesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">createBalanceOrder</a>({ ...params }) -> BrevoApi.CreateBalanceOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns created order
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.createBalanceOrder({
    pid: "pid",
    amount: 1.1,
    balanceDefinitionId: "balanceDefinitionId",
    contactId: 1,
    dueAt: "dueAt",
    source: "source"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateBalanceOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">getSubscriptionBalances</a>({ ...params }) -> BrevoApi.GetSubscriptionBalancesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns subscription balances
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.getSubscriptionBalances({
    pid: "pid",
    cid: "cid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetSubscriptionBalancesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">createSubscriptionBalances</a>({ ...params }) -> BrevoApi.PostLoyaltyBalanceProgramsPidSubscriptionsCidBalancesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a balance for a contact
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.createSubscriptionBalances({
    pid: "pid",
    cid: "cid",
    balanceDefinitionId: "balanceDefinitionId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostLoyaltyBalanceProgramsPidSubscriptionsCidBalancesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">getTransactionHistoryApi</a>({ ...params }) -> BrevoApi.GetLoyaltyBalanceProgramsPidTransactionHistoryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns transaction history
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.getTransactionHistoryApi({
    pid: "pid",
    contact_id: 1,
    balance_definition_id: "balance_definition_id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetLoyaltyBalanceProgramsPidTransactionHistoryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">beginTransaction</a>({ ...params }) -> BrevoApi.Transaction</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates new transaction and returns information
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.beginTransaction({
    pid: "pid",
    amount: 1.1,
    balanceDefinitionId: "balanceDefinitionId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.BeginTransactionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">cancelTransaction</a>({ ...params }) -> BrevoApi.Transaction</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancels transaction
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.cancelTransaction({
    pid: "pid",
    tid: "tid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CancelTransactionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.balance.<a href="/src/api/resources/balance/client/Client.ts">completeTransaction</a>({ ...params }) -> BrevoApi.Transaction</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Completes transaction
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.balance.completeTransaction({
    pid: "pid",
    tid: "tid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CompleteTransactionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `BalanceClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Program
<details><summary><code>client.program.<a href="/src/api/resources/program/client/Client.ts">getLpList</a>({ ...params }) -> BrevoApi.GetLpListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns list of loyalty programs
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.program.getLpList();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetLpListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProgramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.program.<a href="/src/api/resources/program/client/Client.ts">createNewLp</a>({ ...params }) -> BrevoApi.LoyaltyProgram</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates loyalty program
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.program.createNewLp({
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateNewLpRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProgramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.program.<a href="/src/api/resources/program/client/Client.ts">getLoyaltyProgramInfo</a>({ ...params }) -> BrevoApi.LoyaltyProgram</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns loyalty program
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.program.getLoyaltyProgramInfo({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetLoyaltyProgramInfoRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProgramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.program.<a href="/src/api/resources/program/client/Client.ts">updateLoyaltyProgram</a>({ ...params }) -> BrevoApi.LoyaltyProgram</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates loyalty program
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.program.updateLoyaltyProgram({
    pid: "pid",
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateLoyaltyProgramRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProgramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.program.<a href="/src/api/resources/program/client/Client.ts">deleteLoyaltyProgram</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes Loyalty Program
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.program.deleteLoyaltyProgram({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteLoyaltyProgramRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProgramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.program.<a href="/src/api/resources/program/client/Client.ts">partiallyUpdateLoyaltyProgram</a>({ ...params }) -> BrevoApi.LoyaltyProgram</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Partially updates loyalty program
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.program.partiallyUpdateLoyaltyProgram({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PartiallyUpdateLoyaltyProgramRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProgramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.program.<a href="/src/api/resources/program/client/Client.ts">getParameterSubscriptionInfo</a>({ ...params }) -> BrevoApi.GetParameterSubscriptionInfoResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get Information of balances, tiers, rewards and subscription members for a subscription
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.program.getParameterSubscriptionInfo({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetParameterSubscriptionInfoRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProgramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.program.<a href="/src/api/resources/program/client/Client.ts">publishLoyaltyProgram</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Publishes loyalty program
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.program.publishLoyaltyProgram({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PublishLoyaltyProgramRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProgramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.program.<a href="/src/api/resources/program/client/Client.ts">subscribeMemberToASubscription</a>({ ...params }) -> BrevoApi.SubscribeMemberToASubscriptionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add member to a subscription
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.program.subscribeMemberToASubscription({
    pid: "pid",
    memberContactIds: [1]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SubscribeMemberToASubscriptionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProgramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.program.<a href="/src/api/resources/program/client/Client.ts">deleteContactMembers</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes member from a subscription
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.program.deleteContactMembers({
    pid: "pid",
    memberContactIds: "memberContactIds"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteContactMembersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProgramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.program.<a href="/src/api/resources/program/client/Client.ts">subscribeToLoyaltyProgram</a>({ ...params }) -> BrevoApi.SubscribeToLoyaltyProgramResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Subscribes to a loyalty program
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.program.subscribeToLoyaltyProgram({
    pid: "pid",
    contactId: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SubscribeToLoyaltyProgramRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProgramClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Reward
<details><summary><code>client.reward.<a href="/src/api/resources/reward/client/Client.ts">getCodeCount</a>({ ...params }) -> BrevoApi.GetCodeCountResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get code count
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.reward.getCodeCount({
    pid: "pid",
    cpid: "cpid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCodeCountRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reward.<a href="/src/api/resources/reward/client/Client.ts">getRewardPageApi</a>({ ...params }) -> BrevoApi.GetLoyaltyOfferProgramsPidOffersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a reward page
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.reward.getRewardPageApi({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetLoyaltyOfferProgramsPidOffersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reward.<a href="/src/api/resources/reward/client/Client.ts">createReward</a>({ ...params }) -> BrevoApi.CreateRewardResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new reward in the loyalty program.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.reward.createReward({
    pid: "pid",
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateRewardRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reward.<a href="/src/api/resources/reward/client/Client.ts">createVoucher</a>({ ...params }) -> BrevoApi.CreateVoucherResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a voucher and attribute it to a specific membership.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.reward.createVoucher({
    pid: "pid",
    rewardId: "rewardId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateVoucherRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reward.<a href="/src/api/resources/reward/client/Client.ts">redeemVoucher</a>({ ...params }) -> BrevoApi.Redeem</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a request to redeem a voucher.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.reward.redeemVoucher({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.RedeemVoucherRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reward.<a href="/src/api/resources/reward/client/Client.ts">completeRedeemTransaction</a>({ ...params }) -> BrevoApi.Redeem</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Completes voucher redeem request.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.reward.completeRedeemTransaction({
    pid: "pid",
    tid: "tid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CompleteRedeemTransactionRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reward.<a href="/src/api/resources/reward/client/Client.ts">revokeVouchers</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revoke attributed vouchers.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.reward.revokeVouchers({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.RevokeVouchersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reward.<a href="/src/api/resources/reward/client/Client.ts">validateReward</a>({ ...params }) -> BrevoApi.ValidateRewardResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Validates a reward.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.reward.validateReward({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.ValidateRewardRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reward.<a href="/src/api/resources/reward/client/Client.ts">getRewardInformation</a>({ ...params }) -> BrevoApi.GetLoyaltyOfferProgramsPidRewardsRidResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns reward information.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.reward.getRewardInformation({
    pid: "pid",
    rid: "rid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetLoyaltyOfferProgramsPidRewardsRidRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reward.<a href="/src/api/resources/reward/client/Client.ts">getVoucherForAContact</a>({ ...params }) -> BrevoApi.GetLoyaltyOfferProgramsPidVouchersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get voucher for a contact
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.reward.getVoucherForAContact({
    pid: "pid",
    contactId: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetLoyaltyOfferProgramsPidVouchersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `RewardClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Tier
<details><summary><code>client.tier.<a href="/src/api/resources/tier/client/Client.ts">addSubscriptionToTier</a>({ ...params }) -> BrevoApi.AddSubscriptionToTierResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Manually assigns a tier to a specific membership.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tier.addSubscriptionToTier({
    pid: "pid",
    cid: "cid",
    tid: "tid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.AddSubscriptionToTierRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TierClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tier.<a href="/src/api/resources/tier/client/Client.ts">getListOfTierGroups</a>({ ...params }) -> BrevoApi.GetListOfTierGroupsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the list of tier groups defined within the loyalty program.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tier.getListOfTierGroups({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetListOfTierGroupsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TierClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tier.<a href="/src/api/resources/tier/client/Client.ts">createTierGroup</a>({ ...params }) -> BrevoApi.TierGroup</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new tier group in a loyalty program. *(The changes will take effect with the next publication of the loyalty program)*
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tier.createTierGroup({
    pid: "pid",
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateTierGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TierClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tier.<a href="/src/api/resources/tier/client/Client.ts">getTierGroup</a>({ ...params }) -> BrevoApi.TierGroup</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns tier group information.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tier.getTierGroup({
    pid: "pid",
    gid: "gid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetTierGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TierClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tier.<a href="/src/api/resources/tier/client/Client.ts">updateTierGroup</a>({ ...params }) -> BrevoApi.TierGroup</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates a tier group from a loyalty program. *(The changes will take effect with the next publication of the loyalty program)*
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tier.updateTierGroup({
    pid: "pid",
    gid: "gid",
    downgradeStrategy: "real_time",
    name: "name",
    tierOrder: ["tierOrder"],
    upgradeStrategy: "real_time"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateTierGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TierClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tier.<a href="/src/api/resources/tier/client/Client.ts">deleteTierGroup</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes a tier group from a loyalty program. *(The changes will take effect with the next publication of the loyalty program)*
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tier.deleteTierGroup({
    pid: "pid",
    gid: "gid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteTierGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TierClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tier.<a href="/src/api/resources/tier/client/Client.ts">createTierForTierGroup</a>({ ...params }) -> BrevoApi.Tier</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new tier in a loyalty program tier group. *(The changes will take effect with the next publication of the loyalty program)*
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tier.createTierForTierGroup({
    pid: "pid",
    gid: "gid",
    accessConditions: [{}],
    name: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateTierForTierGroupRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TierClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tier.<a href="/src/api/resources/tier/client/Client.ts">getLoyaltyProgramTier</a>({ ...params }) -> BrevoApi.GetLoyaltyProgramTierResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the list of tiers defined within the loyalty program.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tier.getLoyaltyProgramTier({
    pid: "pid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetLoyaltyProgramTierRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TierClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tier.<a href="/src/api/resources/tier/client/Client.ts">updateTier</a>({ ...params }) -> BrevoApi.Tier</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Modifies an existing tier for the specified tier group *(The changes will take effect with the next publication of the loyalty program)*
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tier.updateTier({
    pid: "pid",
    tid: "tid",
    accessConditions: [{}],
    name: "name",
    tierRewards: [{}]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateTierRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TierClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tier.<a href="/src/api/resources/tier/client/Client.ts">deleteTier</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes a tier from a loyalty program tier group. *(The changes will take effect with the next publication of the loyalty program)*
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tier.deleteTier({
    pid: "pid",
    tid: "tid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteTierRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TierClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## EmailCampaigns
<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">getEmailCampaigns</a>({ ...params }) -> BrevoApi.GetEmailCampaignsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
The response payload for this endpoint has changed

You now need to specify which type of statistics you would like to retrieve. For more information visit [this page](https://developers.brevo.com/changelog/get-all-marketing-campaigns).
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.getEmailCampaigns();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetEmailCampaignsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">createEmailCampaign</a>({ ...params }) -> BrevoApi.CreateEmailCampaignResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.createEmailCampaign({
    name: "Newsletter - May 2017",
    sender: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateEmailCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">uploadImageToGallery</a>({ ...params }) -> BrevoApi.UploadImageToGalleryResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.uploadImageToGallery({
    imageUrl: "https://somedomain.com/image1.jpg"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UploadImageToGalleryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">getEmailCampaign</a>({ ...params }) -> BrevoApi.GetEmailCampaignResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.getEmailCampaign({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetEmailCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">updateEmailCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.updateEmailCampaign({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateEmailCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">deleteEmailCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.deleteEmailCampaign({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteEmailCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">getAbTestCampaignResult</a>({ ...params }) -> BrevoApi.GetAbTestCampaignResultResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Obtain winning version of an A/B test email campaign
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.getAbTestCampaignResult({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetAbTestCampaignResultRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">emailExportRecipients</a>({ ...params }) -> BrevoApi.EmailExportRecipientsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.emailExportRecipients({
    campaignId: 1000000,
    recipientsType: "all"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.EmailExportRecipientsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">sendEmailCampaignNow</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.sendEmailCampaignNow({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendEmailCampaignNowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">sendReport</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A PDF will be sent to the specified email addresses
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.sendReport({
    campaignId: 1000000,
    body: {
        email: {
            body: "Please find attached the report of our last email campaign.",
            to: ["jim.suehan@example.com"]
        }
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendReportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">sendTestEmail</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.sendTestEmail({
    campaignId: 1000000,
    body: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendTestEmailRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">getSharedTemplateUrl</a>({ ...params }) -> BrevoApi.GetSharedTemplateUrlResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a unique URL to share & import an email template from one Brevo account to another.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.getSharedTemplateUrl({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetSharedTemplateUrlRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.emailCampaigns.<a href="/src/api/resources/emailCampaigns/client/Client.ts">updateCampaignStatus</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.emailCampaigns.updateCampaignStatus({
    campaignId: 1000000,
    body: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateCampaignStatusRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmailCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## SmsCampaigns
<details><summary><code>client.smsCampaigns.<a href="/src/api/resources/smsCampaigns/client/Client.ts">getSmsCampaigns</a>({ ...params }) -> BrevoApi.GetSmsCampaignsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.smsCampaigns.getSmsCampaigns();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetSmsCampaignsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SmsCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.<a href="/src/api/resources/smsCampaigns/client/Client.ts">createSmsCampaign</a>({ ...params }) -> BrevoApi.CreateSmsCampaignResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.smsCampaigns.createSmsCampaign({
    content: "Get a discount by visiting our NY store and saying : Happy Spring!",
    name: "Spring Promo Code",
    sender: "MyShop"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateSmsCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SmsCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.<a href="/src/api/resources/smsCampaigns/client/Client.ts">getSmsCampaign</a>({ ...params }) -> BrevoApi.GetSmsCampaignResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.smsCampaigns.getSmsCampaign({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetSmsCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SmsCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.<a href="/src/api/resources/smsCampaigns/client/Client.ts">updateSmsCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.smsCampaigns.updateSmsCampaign({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateSmsCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SmsCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.<a href="/src/api/resources/smsCampaigns/client/Client.ts">deleteSmsCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.smsCampaigns.deleteSmsCampaign({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteSmsCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SmsCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.<a href="/src/api/resources/smsCampaigns/client/Client.ts">requestSmsRecipientExport</a>({ ...params }) -> BrevoApi.RequestSmsRecipientExportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

It returns the background process ID which on completion calls the notify URL that you have set in the input.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.smsCampaigns.requestSmsRecipientExport({
    campaignId: 1000000,
    recipientsType: "all"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.RequestSmsRecipientExportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SmsCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.<a href="/src/api/resources/smsCampaigns/client/Client.ts">sendSmsCampaignNow</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.smsCampaigns.sendSmsCampaignNow({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendSmsCampaignNowRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SmsCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.<a href="/src/api/resources/smsCampaigns/client/Client.ts">sendSmsReport</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send report of Sent and Archived campaign, to the specified email addresses, with respective data and a pdf attachment in detail.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.smsCampaigns.sendSmsReport({
    campaignId: 1000000,
    body: {
        email: {
            body: "Please find attached the report of our last email campaign.",
            to: ["jim.suehan@example.com"]
        }
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendSmsReportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SmsCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.<a href="/src/api/resources/smsCampaigns/client/Client.ts">sendTestSms</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.smsCampaigns.sendTestSms({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendTestSmsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SmsCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.smsCampaigns.<a href="/src/api/resources/smsCampaigns/client/Client.ts">updateSmsCampaignStatus</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.smsCampaigns.updateSmsCampaignStatus({
    campaignId: 1000000,
    body: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateSmsCampaignStatusRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SmsCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## WhatsAppCampaigns
<details><summary><code>client.whatsAppCampaigns.<a href="/src/api/resources/whatsAppCampaigns/client/Client.ts">getWhatsAppCampaigns</a>({ ...params }) -> BrevoApi.GetWhatsAppCampaignsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.whatsAppCampaigns.getWhatsAppCampaigns();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetWhatsAppCampaignsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WhatsAppCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.whatsAppCampaigns.<a href="/src/api/resources/whatsAppCampaigns/client/Client.ts">createWhatsAppCampaign</a>({ ...params }) -> BrevoApi.CreateWhatsAppCampaignResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
You can use this API for WhatsApp only if you have setup your WhatsApp account on Brevo platform. To setup your WhatsApp account, follow the steps in the guide below.

[Activating Whatsapp](https://developers.brevo.com/docs/whatsapp-campaigns-1) in your account
</Note>

<Note>
This API requires the List and Segment ids as recipients in Body params. You can use the below Contact endpoints to get the required information.

[Get all the Lists](https://developers.brevo.com/reference/getlists-1)

[Get all the Segments](https://developers.brevo.com/reference/getsegments)
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.whatsAppCampaigns.createWhatsAppCampaign({
    name: "Test Campaign",
    recipients: {},
    scheduledAt: "2017-06-01T12:30:00+02:00",
    templateId: 19
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateWhatsAppCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WhatsAppCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.whatsAppCampaigns.<a href="/src/api/resources/whatsAppCampaigns/client/Client.ts">getWhatsAppConfig</a>() -> BrevoApi.GetWhatsAppConfigResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
You can use this API for WhatsApp only if you have setup your WhatsApp account on Brevo platform. To setup your WhatsApp account, follow the steps in the guide below.

[Activating WhatsApp](https://developers.brevo.com/docs/whatsapp-campaigns-1) in your account
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.whatsAppCampaigns.getWhatsAppConfig();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `WhatsAppCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.whatsAppCampaigns.<a href="/src/api/resources/whatsAppCampaigns/client/Client.ts">createWhatsAppTemplate</a>({ ...params }) -> BrevoApi.CreateWhatsAppTemplateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
You can use this API for WhatsApp only if you have setup your WhatsApp account on Brevo platform. To setup your WhatsApp account, follow the steps in the guide below.

[Activating WhatsApp](https://developers.brevo.com/docs/whatsapp-campaigns-1) in your account
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.whatsAppCampaigns.createWhatsAppTemplate({
    bodyText: "making it look like readable English",
    category: "MARKETING",
    language: "en",
    name: "Test template"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateWhatsAppTemplateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WhatsAppCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.whatsAppCampaigns.<a href="/src/api/resources/whatsAppCampaigns/client/Client.ts">getWhatsAppTemplates</a>({ ...params }) -> BrevoApi.GetWhatsAppTemplatesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.whatsAppCampaigns.getWhatsAppTemplates();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetWhatsAppTemplatesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WhatsAppCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.whatsAppCampaigns.<a href="/src/api/resources/whatsAppCampaigns/client/Client.ts">sendWhatsAppTemplateApproval</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
You can use this API for WhatsApp only if you have setup your WhatsApp account on Brevo platform. To setup your WhatsApp account, follow the steps in the guide below.

[Activating WhatsApp](https://developers.brevo.com/docs/whatsapp-campaigns-1) in your account
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.whatsAppCampaigns.sendWhatsAppTemplateApproval({
    templateId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendWhatsAppTemplateApprovalRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WhatsAppCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.whatsAppCampaigns.<a href="/src/api/resources/whatsAppCampaigns/client/Client.ts">getWhatsAppCampaign</a>({ ...params }) -> BrevoApi.GetWhatsAppCampaignResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
You can use this API for WhatsApp only if you have setup your WhatsApp account on Brevo platform. To setup your WhatsApp account, follow the steps in the guide below.

[Activating Whatsapp](https://developers.brevo.com/docs/whatsapp-campaigns-1) in your account
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.whatsAppCampaigns.getWhatsAppCampaign({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetWhatsAppCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WhatsAppCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.whatsAppCampaigns.<a href="/src/api/resources/whatsAppCampaigns/client/Client.ts">updateWhatsAppCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
You can use this API for WhatsApp only if you have setup your WhatsApp account on Brevo platform. To setup your WhatsApp account, follow the steps in the guide below.

[Activating Whatsapp](https://developers.brevo.com/docs/whatsapp-campaigns-1) in your account
</Note>

<Note>
This API requires the List and Segment ids as recipients in Body params. You can use the below Contact endpoints to get the required information.

[Get all the Lists](https://developers.brevo.com/reference/getlists-1)

[Get all the Segments](https://developers.brevo.com/reference/getsegments)
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.whatsAppCampaigns.updateWhatsAppCampaign({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateWhatsAppCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WhatsAppCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.whatsAppCampaigns.<a href="/src/api/resources/whatsAppCampaigns/client/Client.ts">deleteWhatsAppCampaign</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.whatsAppCampaigns.deleteWhatsAppCampaign({
    campaignId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteWhatsAppCampaignRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WhatsAppCampaignsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Companies
<details><summary><code>client.companies.<a href="/src/api/resources/companies/client/Client.ts">getAllCompanies</a>({ ...params }) -> BrevoApi.GetCompaniesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.companies.getAllCompanies();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCompaniesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.companies.<a href="/src/api/resources/companies/client/Client.ts">createACompany</a>({ ...params }) -> BrevoApi.PostCompaniesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.companies.createACompany({
    name: "company"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCompaniesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.companies.<a href="/src/api/resources/companies/client/Client.ts">importCompaniesCreationAndUpdation</a>({ ...params }) -> BrevoApi.PostCompaniesImportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Import companies from a CSV file with mapping options.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.companies.importCompaniesCreationAndUpdation({});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCompaniesImportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.companies.<a href="/src/api/resources/companies/client/Client.ts">linkAndUnlinkCompanyWithContactAndDeal</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.companies.linkAndUnlinkCompanyWithContactAndDeal({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PatchCompaniesLinkUnlinkIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.companies.<a href="/src/api/resources/companies/client/Client.ts">getACompany</a>({ ...params }) -> BrevoApi.Company</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.companies.getACompany({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCompaniesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.companies.<a href="/src/api/resources/companies/client/Client.ts">deleteACompany</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.companies.deleteACompany({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteCompaniesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.companies.<a href="/src/api/resources/companies/client/Client.ts">updateACompany</a>({ ...params }) -> BrevoApi.Company</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.companies.updateACompany({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PatchCompaniesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.companies.<a href="/src/api/resources/companies/client/Client.ts">createACompanyDealAttribute</a>({ ...params }) -> BrevoApi.PostCrmAttributesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.companies.createACompanyDealAttribute({
    attributeType: "text",
    label: "Attribute Label",
    objectType: "companies"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCrmAttributesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.companies.<a href="/src/api/resources/companies/client/Client.ts">getCompanyAttributes</a>() -> BrevoApi.GetCrmAttributesCompaniesResponseItem[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.companies.getCompanyAttributes();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Deals
<details><summary><code>client.deals.<a href="/src/api/resources/deals/client/Client.ts">getDealAttributes</a>() -> BrevoApi.GetCrmAttributesDealsResponseItem[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deals.getDealAttributes();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `DealsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deals.<a href="/src/api/resources/deals/client/Client.ts">getAllDeals</a>({ ...params }) -> BrevoApi.GetCrmDealsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deals.getAllDeals();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCrmDealsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DealsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deals.<a href="/src/api/resources/deals/client/Client.ts">createADeal</a>({ ...params }) -> BrevoApi.PostCrmDealsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deals.createADeal({
    name: "Deal: Connect with company"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCrmDealsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DealsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deals.<a href="/src/api/resources/deals/client/Client.ts">importDealsCreationAndUpdation</a>({ ...params }) -> BrevoApi.PostCrmDealsImportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Import deals from a CSV file with mapping options.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deals.importDealsCreationAndUpdation({});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCrmDealsImportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DealsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deals.<a href="/src/api/resources/deals/client/Client.ts">linkAndUnlinkADealWithContactsAndCompanies</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deals.linkAndUnlinkADealWithContactsAndCompanies({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PatchCrmDealsLinkUnlinkIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DealsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deals.<a href="/src/api/resources/deals/client/Client.ts">getADeal</a>({ ...params }) -> BrevoApi.Deal</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deals.getADeal({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCrmDealsIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DealsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deals.<a href="/src/api/resources/deals/client/Client.ts">deleteADeal</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deals.deleteADeal({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteCrmDealsIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DealsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deals.<a href="/src/api/resources/deals/client/Client.ts">updateADeal</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deals.updateADeal({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PatchCrmDealsIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DealsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deals.<a href="/src/api/resources/deals/client/Client.ts">getPipelineStages</a>() -> BrevoApi.Pipeline</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint is deprecated. Prefer /crm/pipeline/details/{pipelineID} instead.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deals.getPipelineStages();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `DealsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deals.<a href="/src/api/resources/deals/client/Client.ts">getAllPipelines</a>() -> BrevoApi.Pipelines</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deals.getAllPipelines();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `DealsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deals.<a href="/src/api/resources/deals/client/Client.ts">getAPipeline</a>({ ...params }) -> BrevoApi.Pipelines</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deals.getAPipeline({
    pipelineID: "pipelineID"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCrmPipelineDetailsPipelineIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DealsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Files
<details><summary><code>client.files.<a href="/src/api/resources/files/client/Client.ts">getAllFiles</a>({ ...params }) -> BrevoApi.FileData[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.files.getAllFiles();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCrmFilesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FilesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="/src/api/resources/files/client/Client.ts">uploadAFile</a>({ ...params }) -> BrevoApi.FileData</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.files.uploadAFile({
    file: fs.createReadStream("/path/to/your/file")
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCrmFilesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FilesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="/src/api/resources/files/client/Client.ts">downloadAFile</a>({ ...params }) -> BrevoApi.GetCrmFilesIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.files.downloadAFile({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCrmFilesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FilesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="/src/api/resources/files/client/Client.ts">deleteAFile</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.files.deleteAFile({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteCrmFilesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FilesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.files.<a href="/src/api/resources/files/client/Client.ts">getFileDetails</a>({ ...params }) -> BrevoApi.FileData</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.files.getFileDetails({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCrmFilesIdDataRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FilesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Notes
<details><summary><code>client.notes.<a href="/src/api/resources/notes/client/Client.ts">getAllNotes</a>({ ...params }) -> BrevoApi.Note[]</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.notes.getAllNotes();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCrmNotesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `NotesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notes.<a href="/src/api/resources/notes/client/Client.ts">createANote</a>({ ...params }) -> BrevoApi.PostCrmNotesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.notes.createANote({
    text: "In communication with client_dev for resolution of queries."
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.NoteData` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `NotesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notes.<a href="/src/api/resources/notes/client/Client.ts">getANote</a>({ ...params }) -> BrevoApi.Note</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.notes.getANote({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCrmNotesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `NotesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notes.<a href="/src/api/resources/notes/client/Client.ts">deleteANote</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.notes.deleteANote({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteCrmNotesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `NotesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notes.<a href="/src/api/resources/notes/client/Client.ts">updateANote</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.notes.updateANote({
    id: "id",
    body: {
        text: "In communication with client_dev for resolution of queries."
    }
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PatchCrmNotesIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `NotesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Tasks
<details><summary><code>client.tasks.<a href="/src/api/resources/tasks/client/Client.ts">getAllTasks</a>({ ...params }) -> BrevoApi.GetCrmTasksResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tasks.getAllTasks({
    sortBy: "name"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCrmTasksRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TasksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="/src/api/resources/tasks/client/Client.ts">createATask</a>({ ...params }) -> BrevoApi.PostCrmTasksResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tasks.createATask({
    date: "2021-11-01T17:44:54Z",
    name: "Task: Connect with client_dev",
    taskTypeId: "61a5cd07ca1347c82306ad09"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PostCrmTasksRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TasksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="/src/api/resources/tasks/client/Client.ts">getATask</a>({ ...params }) -> BrevoApi.Task</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tasks.getATask({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetCrmTasksIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TasksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="/src/api/resources/tasks/client/Client.ts">deleteATask</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tasks.deleteATask({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteCrmTasksIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TasksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="/src/api/resources/tasks/client/Client.ts">updateATask</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tasks.updateATask({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.PatchCrmTasksIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TasksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="/src/api/resources/tasks/client/Client.ts">getAllTaskTypes</a>() -> BrevoApi.GetCrmTasktypesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.tasks.getAllTaskTypes();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `TasksClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## TransactionalWhatsApp
<details><summary><code>client.transactionalWhatsApp.<a href="/src/api/resources/transactionalWhatsApp/client/Client.ts">sendWhatsappMessage</a>({ ...params }) -> BrevoApi.SendWhatsappMessageResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>You can use this API for WhatsApp only if you have setup your WhatsApp account on Brevo platform. To setup your WhatsApp account, follow the steps in the guide below. [Activating Whatsapp](https://developers.brevo.com/docs/whatsapp-campaigns-1) in your account</Note>
This endpoint is used to send a WhatsApp message. <br/>(**The first message you send using the API must contain a Template ID. You must create a template on WhatsApp on the Brevo platform to fetch the Template ID.**)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalWhatsApp.sendWhatsappMessage({
    contactNumbers: ["contactNumbers"],
    senderNumber: "senderNumber",
    templateId: 123
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendWhatsappMessageRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalWhatsAppClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalWhatsApp.<a href="/src/api/resources/transactionalWhatsApp/client/Client.ts">getWhatsappEventReport</a>({ ...params }) -> BrevoApi.GetWhatsappEventReportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will show the unaggregated statistics for WhatsApp activity (30 days by default if `startDate` and `endDate` or `days` is not passed. The date range can not exceed 90 days)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalWhatsApp.getWhatsappEventReport();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetWhatsappEventReportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalWhatsAppClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## TransactionalEmails
<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">getTransacBlockedContacts</a>({ ...params }) -> BrevoApi.GetTransacBlockedContactsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.getTransacBlockedContacts();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetTransacBlockedContactsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">unblockOrResubscribeATransactionalContact</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.unblockOrResubscribeATransactionalContact({
    email: "email"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteSmtpBlockedContactsEmailRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">getBlockedDomains</a>() -> BrevoApi.GetBlockedDomainsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the list of blocked domains
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.getBlockedDomains();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">blockNewDomain</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Blocks a new domain in order to avoid messages being sent to the same
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.blockNewDomain({
    domain: "example.com"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.BlockNewDomainRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">deleteBlockedDomain</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Unblocks an existing domain from the list of blocked domains
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.deleteBlockedDomain({
    domain: "domain"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteBlockedDomainRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">deleteHardbounces</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete hardbounces. To use carefully (e.g. in case of temporary ISP failures)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.deleteHardbounces();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteHardbouncesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">sendTransacEmail</a>({ ...params }) -> BrevoApi.SendTransacEmailResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.sendTransacEmail({
    htmlContent: "<html><head></head><body><p>Hello,</p>This is my first transactional email sent from Brevo.</p></body></html>",
    sender: {
        email: "hello@brevo.com",
        name: "Alex from Brevo"
    },
    subject: "Hello from Brevo!",
    to: [{
            email: "johndoe@example.com",
            name: "John Doe"
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendTransacEmailRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">deleteScheduledEmailById</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete scheduled batch of emails by batchId or single scheduled email by messageId
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.deleteScheduledEmailById({
    identifier: "4320f270-a4e3-4a2e-b591-edfe30a5e627"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteScheduledEmailByIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">getScheduledEmailById</a>({ ...params }) -> BrevoApi.GetScheduledEmailByIdResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Fetch scheduled batch of emails by batchId or single scheduled email by messageId (Can retrieve data upto 30 days old)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.getScheduledEmailById({
    identifier: "4320f270-a4e3-4a2e-b591-edfe30a5e627",
    startDate: "2022-02-02",
    endDate: "2022-03-02"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetScheduledEmailByIdRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">getTransacEmailsList</a>({ ...params }) -> BrevoApi.GetTransacEmailsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will show the list of emails for past 30 days by default. To retrieve emails before that time, please pass startDate and endDate in query filters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.getTransacEmailsList();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetTransacEmailsListRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">getTransacEmailContent</a>({ ...params }) -> BrevoApi.GetTransacEmailContentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note title="How to get uuid?">
You can get the uuid using either of the following methods:

Send a GET request to https://api.brevo.com/v3/smtp/emails and pass the message_id in the url. Use your api-key to authenticate the request and you will get your uuid as a response.

The uuid can also be fetched from the transactional logs page in your Brevo account, from the address URL.
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.getTransacEmailContent({
    uuid: "uuid"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetTransacEmailContentRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">deleteAnSmtpTransactionalLog</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.deleteAnSmtpTransactionalLog({
    identifier: "identifier"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteSmtpLogIdentifierRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">getAggregatedSmtpReport</a>({ ...params }) -> BrevoApi.GetAggregatedSmtpReportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will show the aggregated stats for past 90 days by default if `startDate` and `endDate` OR `days` is not passed. The date range can not exceed 90 days
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.getAggregatedSmtpReport();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetAggregatedSmtpReportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">getEmailEventReport</a>({ ...params }) -> BrevoApi.GetEmailEventReportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint will show the aggregated stats for past 30 days by default if `startDate` and `endDate` OR `days` is not passed. The date range can not exceed 90 days
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.getEmailEventReport();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetEmailEventReportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">getSmtpReport</a>({ ...params }) -> BrevoApi.GetSmtpReportResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.getSmtpReport();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetSmtpReportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">postPreviewSmtpEmailTemplates</a>({ ...params }) -> BrevoApi.PostPreviewSmtpEmailTemplatesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.postPreviewSmtpEmailTemplates({
    "key": "value"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `unknown` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">getSmtpTemplates</a>({ ...params }) -> BrevoApi.GetSmtpTemplatesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.getSmtpTemplates();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetSmtpTemplatesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">createSmtpTemplate</a>({ ...params }) -> BrevoApi.CreateSmtpTemplateResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.createSmtpTemplate({
    sender: {},
    subject: "Thanks for your purchase !",
    templateName: "Order Confirmation - EN"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.CreateSmtpTemplateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">getSmtpTemplate</a>({ ...params }) -> BrevoApi.GetSmtpTemplateOverview</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.getSmtpTemplate({
    templateId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetSmtpTemplateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">updateSmtpTemplate</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.updateSmtpTemplate({
    templateId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.UpdateSmtpTemplateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">deleteSmtpTemplate</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.deleteSmtpTemplate({
    templateId: 1000000
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.DeleteSmtpTemplateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalEmails.<a href="/src/api/resources/transactionalEmails/client/Client.ts">sendTestTemplate</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalEmails.sendTestTemplate({
    templateId: 1000000,
    body: {}
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendTestTemplateRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalEmailsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## TransactionalSms
<details><summary><code>client.transactionalSms.<a href="/src/api/resources/transactionalSms/client/Client.ts">sendAsyncTransactionalSms</a>({ ...params }) -> BrevoApi.SendAsyncTransactionalSmsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

<Note>
If the user includes stop code in the Transactional SMS, then it will be switched to Marketing SMS automatically and it will be interpreted as a Marketing SMS. To send Transactional SMS as Transactional, it is important not to use stop code.

Note: For adding a stop code, client has to add reply STOP to [STOP_CODE] and the [STOP_CODE] will be replaced with the number.
</Note>

<Note title="For end users in France">
Transactional SMS can be sent at any time without time restrictions. However, if a message is categorized as Marketing, it must adhere to specific time restrictions. Messages sent outside of these restricted hours will experience delays and will be processed during allowable times. Specifically, Marketing SMS cannot be processed between 10pm and 8am, on Sundays, and on French public holidays.
</Note>
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalSms.sendAsyncTransactionalSms({
    recipient: "33689965433",
    sender: "MyShop"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendTransacSms` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalSmsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalSms.<a href="/src/api/resources/transactionalSms/client/Client.ts">sendTransacSms</a>({ ...params }) -> BrevoApi.SendTransacSmsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalSms.sendTransacSms({
    recipient: "33689965433",
    sender: "MyShop"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.SendTransacSms` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalSmsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalSms.<a href="/src/api/resources/transactionalSms/client/Client.ts">getTransacAggregatedSmsReport</a>({ ...params }) -> BrevoApi.GetTransacAggregatedSmsReportResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalSms.getTransacAggregatedSmsReport();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetTransacAggregatedSmsReportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalSmsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalSms.<a href="/src/api/resources/transactionalSms/client/Client.ts">getSmsEvents</a>({ ...params }) -> BrevoApi.GetSmsEventsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalSms.getSmsEvents();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetSmsEventsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalSmsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.transactionalSms.<a href="/src/api/resources/transactionalSms/client/Client.ts">getTransacSmsReport</a>({ ...params }) -> BrevoApi.GetTransacSmsReportResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.transactionalSms.getTransacSmsReport();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetTransacSmsReportRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TransactionalSmsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## SmsTemplates
<details><summary><code>client.smsTemplates.<a href="/src/api/resources/smsTemplates/client/Client.ts">getSmsTemplates</a>({ ...params }) -> BrevoApi.GetSmsTemplatesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.smsTemplates.getSmsTemplates();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `BrevoApi.GetSmsTemplatesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SmsTemplatesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>
