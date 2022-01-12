## Modified PKCE Command Line Tool to Automate Login

This tool demonstrates an Automated Authorization Code Flow with PKCE and Authn



## Usage

```
Edit run.sh
Add
 --client_id
 --okta_org
 --user
 --user
```

## Run

```
npm install
./run.sh
```

You'll get output like this:

```
Created Code Verifier (v): bc7b_fb3a_5576_3569_5b28_3876_4974_3bfe_9793_383d_00b3

Created Code Challenge ($): 6hxXJb5aXMH1Kt7BMsOkOLwqhD5CW0rQJ3IENyrDj6c

Running...
session: 20111jgOZ0pNkOoQTAl70UDI_2_8R9U90f5LnEwQXxuACwxvkQDZ__7

Got code (α): ehCJgNuhboqLspMPpDFT0QQeEx4FrziFp-pMHbeBMEY


Calling /token endpoint with:
client_id: 0oa1ddcipQGRBMQ815d6
code_verifier (v): bc7b_fb3a_5576_3569_5b28_3876_4974_3bfe_9793_383d_00b3
code (α): ehCJgNuhboqLspMPpDFT0QQeEx4FrziFp-pMHbeBMEY

Here is the complete form post that will be sent to the /token endpoint:
{
  grant_type: 'authorization_code',
  redirect_uri: 'http://localhost:8080/redirect',
  client_id: '0oa1ddcipQGRBMQ815d6',
  code: 'ehCJgNuhboqLspMPpDFT0QQeEx4FrziFp-pMHbeBMEY',
  code_verifier: 'bc7b_fb3a_5576_3569_5b28_3876_4974_3bfe_9793_383d_00b3'
}


Got token response:
{
  token_type: 'Bearer',
  expires_in: 3600,
  access_token: 'eyJraWQiOiIwNE45M2l0WnpjMER...',
  scope: 'openid profile email',
  id_token: 'eyJraWQiOiJ...'
}
```


