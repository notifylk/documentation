# Direct Endpoints for Notify.lk SMS Actions

## Send SMS

Use this endpoint directly to send SMS to a contact number.

### _Request_

URL : `https://app.notify.lk/api/v1/send`

Type: `GET` or `POST`

#### _Parameters_

| Key | Required | Value |
| --- | --- | --- |
| `user_id` | YES | User ID from your settings page. |
| `api_key` | YES | API key from your settings page. |
| `sender_id` | YES | Your approved Sender ID. Use “NotifyDEMO” for testing. This one is case sensitive. |
| `to` | YES | The number of the recipient. Should be in the format of 9471XXXXXXX. |
| `message` | YES | The message. Max: 320 chars. |
| `contact_fname` | NO | (Optional) First name of the contact. Will be used while saving the contact. |
| `contact_lname` | NO | (Optional) Last name of the contact. Will be used while saving the contact. |
| `contact_email` | NO | (Optional) Email of the contact. Will be used while saving the contact. |
| `contact_address` | NO | (Optional) Local address of the contact. Will be used while saving the contact. |
| `contact_group` | NO | (Optional) Contact Group Id, if you need to assign the saving contact to a group. |

#### _Response_

You will get a JSON response in a success or a failure attempt.

```
{
 "status": "success",
 "data": "Sent"
}
```

#### _Example Call_

```
https://app.notify.lk/api/v1/status?user_id=[USER_ID]&api_key=[API_KEY]&sender_id=NotifyDEMO&to=[TO]&message=Test
```

Replace `[API_KEY]` and `[USER_ID]` with your account information and `[TO]` with the phone number you need to receive the SMS to. And then visit the URL with your browser.

You can find your account's API information [here](https://app.notify.lk/settings/api-keys) .

## Account Status 

You can use this API endpoint to retrieve account status and the account balance.

### _Request_

URL : `https://app.notify.lk/api/v1/status`

Type: `GET`

#### _Parameters_

| Key | Required | Value |
| --- | --- | --- |
| `user_id` | YES | User ID from your settings page. |
| `api_key` | YES | API key from your settings page. |

#### _Example Call_

```
http://app.notify.lk/api/v1/status?user_id=[USER_ID]&api_key=[API_KEY]
```

Replace `[API_KEY]` and `[USER_ID]` with your account information and `[TO]` with the phone number you need to receive the SMS to. And then visit the URL with your browser.

You can find your account's API information [here](https://app.notify.lk/settings/api-keys) .
