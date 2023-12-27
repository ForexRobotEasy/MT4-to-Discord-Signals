# MT4 to Discord Signals

This code allows you to link your brokerage account with Discord, providing seamless trading notifications and an enhanced trading experience. 

**Developer's Site**: [forexroboteasy.com](https://forexroboteasy.com)

**Development**: Forex Robot Easy Team

## Global Variables

- `discordChannel`: The Discord channel to which notifications will be sent.
- `discordWebhook`: The webhook URL for the Discord channel.
- `sendScreenshot`: A boolean value indicating whether to send a screenshot along with the notification.

## Set Discord Channel

The `SetDiscordChannel` function is used to set the Discord channel and webhook URL.

```mql5
void SetDiscordChannel(string channel, string webhook)
```

## Send Trading Notifications

The `SendNotification` function is used to send trading notifications to the Discord channel.

```mql5
void SendNotification(string message)
```

## Capture Screenshot

The `CaptureScreenshot` function captures and saves a screenshot of the trading platform. It then sends the screenshot to the Discord channel.

```mql5
void CaptureScreenshot()
```

## Filter Notifications

The `FilterNotification` function is used to filter the trading notifications based on user-defined logic.

```mql5
bool FilterNotification(string symbol, ENUM_TRADE_EVENT event)
```

## Trading Events

The `OnTradeEvent` function is called whenever a trading event occurs. It filters the events based on the user-defined logic and sends the appropriate notification. If enabled, it also captures and sends a screenshot.

```mql5
void OnTradeEvent(const MqlTradeEvent& event)
```

## Expert Advisor Settings

- `EnableScreenshot`: A boolean input parameter to enable/disable the screenshot feature.

## Expert Advisor Initialization

The `OnInit` function is called during EA initialization. It initializes the screenshot feature if enabled.

```mql5
int OnInit()
```

## Expert Advisor Deinitialization

The `OnDeinit` function is called during EA deinitialization. It cleans up any necessary resources.

```mql5
void OnDeinit(const int reason)
```

## Expert Advisor Start

The `OnStart` function is called when the EA starts. It sets the Discord channel and webhook URL, attaches the event handler, and sets timers for periodic tasks.

```mql5
void OnStart()
```

## Timer Event

The `OnTimer` function is called periodically based on the timer set in the `OnStart` function. It performs any necessary periodic tasks.

```mql5
void OnTimer()
```

## Product Description

MT4 to Discord Signals is a program developed by Forex Robot Easy Team to link your brokerage account with Discord. It provides seamless trading notifications and enhances your trading experience.

With MT4 to Discord Signals, you can receive real-time trading notifications directly to your Discord channel. Stay updated on order placements, modifications, executions, and closures. Customize the notifications by applying your own filter logic.

The program also offers the option to capture and send screenshots along with the notifications. This feature allows you to share visual representations of your trading activities, providing a comprehensive trading experience.

Please note that Forex Robot Easy is not the official developer of MT4 to Discord Signals. We are showcasing sample code that can work as described in this product. To find the official developer of this product, please refer to MQL5.

For detailed reviews and trading results of this product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/mt4-to-discord-signals-review-enhance-forex-trading-notifications/).
