# Telegram-BotSDK
Telegram Bot API SDK for .NET Developers (Framework / Standard / .Net Core)

> If you are a Microsoft .NET developer using C#, VisualBasic, ASP.NET or other technologies and would like to create a bot on Telegram, Congratulations! you found the right SDK.


### How to use?

```c#
using hShahpouri.Telegram;
using System.Web.Http;

namespace tgioBot.Controllers
{
    public class StartController : ApiController
    {
        // POST: Start/{token}
        [HttpPost("/Start/{token}")]
        public IActionResult Post(string token, [FromBody]Update json)
        {
            if (json == null)
                return BadRequest();

            Bot bot = new Bot(token);
            bot.sendMessage(json.message.chat.id.ToString(), $"Hello <b>{json.message.chat.first_name}</b>!", Bot.ParseMode.HTML, null, null, null, null);

            return Ok();
        }
    }
}

```

Need help? contact me on Telegram : [@hShahpouri](https://t.me/hshahpouri)
