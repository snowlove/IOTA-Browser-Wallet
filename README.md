# IOTA-Browser-Wallet (READ THIS FIRST!!!!)

This is a proof of concept using the iota.lib.js to run a wallet in your browser.

## This is mainly for people to tinker with and play around with different ideas!
## AGAIN READ ABOVE

it should be technically sound, but I will not be held responsible for loss of IOTA should you use it in a browser with malicious extensions.

Security riskes:
* If you're using malicious extensions/addons for your browser it could easily steal your seed.
* I've tried to limit everything to local storage, it still does a few remote connection:
	* https://fonts.googleapis.com/css?family=Lato:300,400,700 (Fonts)
	* https://fonts.gstatic.com/s/lato/v14/1YwB1sO8YE1Lyjf12WNiUA.woff2 (Fonts)
	* https://fonts.gstatic.com/s/lato/v14/H2DMvhDLycM56KNuAtbJYA.woff2 (Fonts)
	* Other than that the only remote connection should be to the node you're connecting to.
* it could be glitchly!

----

Features:
* Pull information on a seed (Balance, Addresses, Transactions)
	* Addresses: Has address been used (true/false) + if address has balance
	* Transactions: Hash + Value + Type + addresses sent to and from (Will ignore bundle replays so total tx may be smaller than the Transactions table)
* Generate Addresses: Generate a single address, or in batches of 25,50,75,100! and automatically attach them to the tangle.
* Seed generator using Knarz code (NOT MATH.RANDOM)
* Decently verbose (will make it more so overtime and add option to turn verbose output off)
* Hide console log