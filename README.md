# apigee-practice-session
Basic authentication

Basic authentication

-> create a new proxy -> with target ->develop -> reflow ->request-> add basic authentication policy 

-> postman -> hostid/proxy ? username = value& password = value

<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<BasicAuthentication continueOnError="false" enabled="true" name="Basic-Authentication-1">
    <DisplayName>Basic Authentication-1</DisplayName>
    <Operation>Encode</Operation>
    <IgnoreUnresolvedVariables>false</IgnoreUnresolvedVariables>
    <User ref="request.queryparam.username"/>
    <Password ref="request.queryparam.password"/>
    <AssignTo createNew="false">request.header.Authorization</AssignTo>
    <Source>request.header.Authorization</Source>
</BasicAuthentication>
