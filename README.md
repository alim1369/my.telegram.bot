## Telegram Bot Api Library

C# library to talk to Telegrams Bot API (https://core.telegram.org/bots/api)

## Usage

```C#
static void testApiAsync()
{
    var Bot = new Telegram.Bot.MyApi("your API access Token");
    var me = await Bot.GetMe();
    System.Console.WriteLine("Hello my name is " + me.FirstName);
    Bot.OnMessage += OnMessage;
    Bot.OnInlineQuery += OnInlineQuery;
    Bot.OnChooseInlineResult += OnChooseInlineResult;
    Bot.Start();
    Bot.WaitToDie();
}
```

see [telegram.bot.examples](https://github.com/MrRoundRobin/telegram.bot.examples)

## Installation

Install as [NuGet package](https://www.nuget.org/packages/Telegram.Bot/):

```
Install-Package Telegram.Bot
```

## API Coverage

There are functions for all available API methods. (2016-01-05) incl. [Inline mode](https://core.telegram.org/bots/api#inline-mode)

Missing: [Making requests when getting updates](https://core.telegram.org/bots/api#making-requests-when-getting-updates)
