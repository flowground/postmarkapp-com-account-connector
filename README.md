# ![LOGO](logo.png) Postmark Account-level **flow**ground Connector

## Description

A generated **flow**ground connector for the Postmark Account-level API (version 0.9.0).

Generated from: https://api.apis.guru/v2/specs/postmarkapp.com/account/0.9.0/swagger.json<br/>
Generated at: 2019-05-07T17:43:44+03:00

## API Description

Postmark makes sending and receiving email
incredibly easy. The Account-level API allows users to
configure all Servers, Domains, and Sender Signatures associated
with an Account.


## Authorization

This API does not require authorization.

## Actions

### List Domains

*Tags:* `Domains API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `count` - _required_ - Number of records to return per request. Max 500.
* `offset` - _required_ - Number of records to skip

### Create a Domain

*Tags:* `Domains API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.

### Delete a Domain

*Tags:* `Domains API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `domainid` - _required_ - The ID for the Domain that should be deleted by the request.

### Get a Domain

*Tags:* `Domains API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `domainid` - _required_ - The ID for the Domain that should be retrieved.

### Update a Domain

*Tags:* `Domains API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `domainid` - _required_ - The ID for the Domain that should be modified by the request.

### Rotate DKIM Key

> Creates a new DKIM key to replace your current key. Until the DNS entries are confirmed,<br/>
> the new values will be in the `DKIMPendingHost` and `DKIMPendingTextValue` fields.<br/>
> After the new DKIM value is verified in DNS, the pending values will migrate to<br/>
> `DKIMTextValue` and `DKIMPendingTextValue` and Postmark will begin to sign emails<br/>
> with the new DKIM key.

*Tags:* `Domains API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `domainid` - _required_ - The ID for the Sender Signature for which a new DKIM Key should be generated.

### Request DNS Verification for DKIM

*Tags:* `Domains API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `domainid` - _required_ - The ID for the Domain for which DKIM DNS records should be verified.

### Request DNS Verification for Return-Path

*Tags:* `Domains API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `domainid` - _required_ - The ID for the Domain for which Return-Path DNS records should be verified.

### Request DNS Verification for SPF

*Tags:* `Domains API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `domainid` - _required_ - The ID for the Domain for which SPF DNS records should be verified.

### List Sender Signatures

*Tags:* `Sender Signatures API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `count` - _required_ - Number of records to return per request. Max 500.
* `offset` - _required_ - Number of records to skip

### Create a Sender Signature

*Tags:* `Sender Signatures API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.

### Delete a Sender Signature

*Tags:* `Sender Signatures API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `signatureid` - _required_ - The ID for the Sender Signature that should be deleted by the request.

### Get a Sender Signature

*Tags:* `Sender Signatures API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `signatureid` - _required_ - The ID for the Sender Signature that should be retrieved.

### Update a Sender Signature

*Tags:* `Sender Signatures API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `signatureid` - _required_ - The ID for the Sender Signature that should be modified by the request.

### Request a new DKIM Key

> Requests a new DKIM key to be created. Until the DNS entries are confirmed,<br/>
> the new values will be in the `DKIMPendingHost` and `DKIMPendingTextValue` fields.<br/>
> After the new DKIM value is verified in DNS, the pending values will migrate to<br/>
> `DKIMTextValue` and `DKIMPendingTextValue` and Postmark will begin to sign emails<br/>
> with the new DKIM key.

*Tags:* `Sender Signatures API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `signatureid` - _required_ - The ID for the Sender Signature for which a new DKIM Key should be generated.

### Resend Signature Confirmation Email

*Tags:* `Sender Signatures API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `signatureid` - _required_ - The ID for the Sender Signature that should have its confirmation email resent.

### Request DNS Verification for SPF

*Tags:* `Sender Signatures API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `signatureid` - _required_ - The ID for the Sender Signature for which SPF DNS records should be verified.

### List servers

*Tags:* `Server Management API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `count` - _required_ - Number of servers to return per request.
* `offset` - _required_ - Number of servers to skip.
* `name` - _optional_ - Filter by a specific server name

### Create a Server

*Tags:* `Server Management API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.

### Delete a Server

*Tags:* `Server Management API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `serverid` - _required_ - The ID of the Server that should be deleted.

### Get a Server

*Tags:* `Server Management API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `serverid` - _required_ - The ID of the Server to get.

### Edit a Server

*Tags:* `Server Management API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.
* `serverid` - _required_ - The ID of the Server to update.

### Push templates from one server to another

*Tags:* `Templates API`

#### Input Parameters
* `X-Postmark-Account-Token` - _required_ - The token associated with the Account on which this request will operate.

## License

**flow**ground :- Telekom iPaaS / postmarkapp-com-account-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
