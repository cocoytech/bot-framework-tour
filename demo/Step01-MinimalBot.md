- Add package dependency for bot builder (must specify version) `dotnet add package Microsoft.Bot.Builder.Integration.AspNet.Core -v 4.3.2`
- In `Startup.Configure()` add `app.UseBotFramework()` **before** `app.Run(...)`
- Try connecting emulator to /api/messages (note that you **must** use http endpoint, **not** https). Observe error about missing registration.
- Add IBot implementation with "Hello world" response, add `services.AddBot<MyBot>()`
- Test again, this will work

## [Compare changes](https://github.com/maxnorth/bot-framework-tour/compare/step-00-new-app...step-01-minimal-bot)