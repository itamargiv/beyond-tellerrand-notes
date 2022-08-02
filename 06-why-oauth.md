# Why do we Even Need OAuth Anyways?

> By: [Aaron Parecki](https://beyondtellerrand.com/events/dusseldorf-2021/speakers/aaron-parecki)
>
> **Video**: https://www.youtube.com/watch?v=uN860I2kGo0

- Security is becoming increasingly important, due to connected devices
  proliferation.
- OAuth is one of the most complicated specs, since it is made of a combination
  of dozens of several different specs themselves.
- OAuth is more than just the sign in with Facebook / google etc. menu.

## A bit of history

- In the past, in order to sign in to a service using other credentials, you had
  to give that application your credentials.
- Even though the 3rd party app only wants to use some of the information form
  your connected account, you still had to give it access to the entirety of
  your account.
- This means you give full trust to that 3rd party app to do the right thing,
  and also to keep your private credentials safe.
- Users still want to share data between applications, but they also want to do
  it safely. To do that, you can define a standard to limit the scope of what
  the 3rd party can do with your account, and for how long. We can liken this to
  a hotel giving a guest a hotel key for a specific room for a specific period
  of time, instead of the master key for al time.

## How does it work?

0. 3rd party app sends some access tokens to an oauth server.
0. OAuth server (on the original app) will require the user to authorize the 3rd
   party app for certain scopes.
0. If the 3rd party app was authorized, the user will be redirected back to the
   3rd party app itself.

## What about 1st party apps?

- Sometimes 1st party apps might need to use oauth in order to provide a
  consistent user experience. For example: The Apple ID can be required from the
  users at various places across apple products, but each dialog looks
  differently.
- Not using OAuth for 1st party apps can lead to phishing attack since these
  dialogs can be easily faked.
- Multi factor auth also doesn't necessarily help here either since you can
  easily type in your access code into the phishing website.
- If you tie in the MFA (multi factor auth) to a domain name, you can prevent
  phishing attacks. But in order to do so, you will still need to use a
  centralized authentication server, which is essentially OAuth.

## Registration and Account Recovery

- Registration and account recovery is an entire subsystem in an app that needs
  to be designed and developed.
- OAuth can help solve this, since the OAuth server will be able to handle the
  registration and account recovery subsystem.
- The same OAuth server can be used for multiple applications as a shared
  accounts service.

## Shared Logins

- Going back to the "sign in with..." buttons example, it is in essence OAuth,
  but it is OAuth + custom logic for each provider.
- To Handle this additional custom logic, we have systems such as OpenID
  connect. to offload the account handling logic.

## The Future

- OAuth is a living specification, and is continuously under development
- There are extensions to the OAuth security protocol to make safe for FinTech
  and other applications.
- The specs themselves also need some cleaning up for legibility and clarity.

## Learn More

* https://oauth.net/      - community space for learning OAuth
* https://oauth.wtf/       - A book by the presenter about OAuth
* https://indieauth.net/  - OAuth for the open web.
