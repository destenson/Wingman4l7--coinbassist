coinbassist
===========

## About ##
This is a node.js application which provides command-line access to [Coinbase]. You can:

  - show current exchange rate
  - check your balance
  - show your current receive address  
  - generate & display a new receive address
  - show buy or sell price (incl. fees) for a given amount of BTC

It will also optionally log all your actions to a text file.  More to come!

You will also of course be able to automatically buy/sell [Bitcoin] (BTC).

## How to Install ##

### node.js & dependencies ###
This needs [node.js] to work, so install that first.  This was tested & developed on v0.10.<i>x</i>.

Then, you will need to install the module dependencies.  Currently that is only [restler], *"an HTTP client library for node.js"*.  After installing node.js, run this command to do it:

	npm install restler

### Coinbase API key ###

You'll have to enable your Coinbase [API key] for this to work; you will of course have to be logged in to do this.  Once you've done that, paste your API key into your config file in the appropriate location.

**WARNING:** If you clone this repo so you can modify it, BE CAREFUL and DO NOT UPLOAD your config file with your API key in it!  This would allow someone to steal the Bitcoins from your Coinbase wallet!  

I personally recommend disabling your API key when you're not using this application as an extra safety measure.

## How to Run ##
For now, this is as simple as:

	node coinbassist.js

## How to Use ##

### Commands ###
You are provided with a command prompt.  Current available commands are:

	help:    gives a complete list of commands and what they do
	rate:    shows their current exchange rate (BTC to USD)
	balance: shows your current account balance (in BTC)
	getaddy: shows your current receive address
	newaddy: generates & displays a new receive address
	buyprice:  shows buy price incl. fees (use: buyprice #)
	sellprice: shows sell price incl. fees (use: sellprice #)
    quit / exit: does what it says on the tin

*The automatic "buy" functionality is currently disabled while I work it into the new prompt interface.*

### Config File ###
This is where you'll put the API key and set other options, like if you want logging on *(set to `true`)* or off *(set to `false`)*.

If you want to just buy BTC and don't care to use the threshold to buy under/at a certain price, just set the theshold config value high enough so it won't matter.  The "min" and "max" values in the config aren't currently used anywhere.

## Origins & Credit Due ##
Initially cloned from [chenosaurus]' [buy.js Gist]; incorporated threshold functionality from [FernandoEscher]'s [fork of same].  I used the JSON config file and REPL-as-command-line from [martindale]'s [coinbase-trader], and I'll probably be using other bits from it in the near future.

Credit goes to [AlliedEnvy] for the clever name.

## License ##
I haven't bothered to formally declare which license this is going to be under, but it's obviously open-source, and it will probably be some flavor of [Creative Commons], or maybe [GPL].

## Donations ##
Like this script?  You can send Bitcoin donations to: `1F7kfMNUNQy8e52RHnQAWYXeaYfzFqHJAZ`

*Quick reference:* $1 USD is currently: <img src="http://btcticker.appspot.com/mtgox/1.00usd.png">

[Bitcoin]: http://bitcoin.org/
[Coinbase]: https://coinbase.com/
[node.js]: http://nodejs.org/
[restler]: https://github.com/danwrong/restler
[API key]: https://coinbase.com/account/integrations
[chenosaurus]: https://gist.github.com/chenosaurus
[buy.js Gist]: https://gist.github.com/chenosaurus/5102546
[FernandoEscher]: https://gist.github.com/FernandoEscher
[fork of same]: https://gist.github.com/FernandoEscher/5103601
[martindale]: https://github.com/martindale
[coinbase-trader]: https://github.com/martindale/coinbase-trader
[AlliedEnvy]: https://github.com/AlliedEnvy
[Creative Commons]: http://creativecommons.org/licenses/
[GPL]: http://www.gnu.org/licenses/licenses.html