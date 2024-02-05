

## MoneyGuard SDK For Xamarin Sample

MoneyGuard SDK For Xamarin allows financial institutions to embed [Moneyguard](https://wimika.ng/moneyguard/) into
their Xamarin applications. 

## Getting Started

1. Obtain a partner Id from Wimika RMS Technologies

2. Implement a REST API endpoint that exposes [Wimika Partner Bank Service API](https://wimika.gitbook.io/wimika-partner-bank-api-documentation/)

3. Embed Wimika Moneyguard in your Android Application

## Usage For Android


### 1) Initialize MoneyGuard 

Initialize Moneyguard. An IBasicSession is an implementation of the methods that support the following Moneyguard
functionality :
 - Credential Compromise Check
 - Create a Typing Profile Recorder
 - Preview a banking transaction before it is processed

```java

Activity activity; //Main Activity
int partnerBankId = <partner-bank-id>; //obtained from Wimika
string sessionToken = <session-token>;//session token that will be passed to Partner Bank REST Service to validate user session 

Task<IBasicSession> session = await MoneyguardSdk.Register(activity, partnerBankId, sessionToken);

```





