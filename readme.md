Hello,

Welcome to my project, feel free to send me an email at nate_km@protonmail.com.

Feel free to send me a Bitcoin Cash donation here (1NLkGPnNbT9iCJ35U9UfsURANtYgNREVtq)
or email me if you want to send me something else and I will respond with an address.

How to use:

  This monitors a users twitter stream (instant) and acts on every
  tweet that It sees. It is currently pointed at the correct one.
  
  ```
  var stream = T.stream('statuses/filter', { follow : '961445378' });
  /* You just need to change the follow ID to point it at someone else */
  ```

  To Get It To Start
  1. You must CD into directory and type "npm install" (make sure npm & node.js is installed). (This will install the necessary dependencies. 
  2. You must give it your API_KEY and Secret on line (6 & 7) from Poloniex to make buys, you must also get your twitter keys here. (as shown below)
  ```
  const API_KEY = '';
  const SECRET = '';
  ```
  
  3. You must go to https://apps.twitter.com/ to get your consumer_key, consumer_secret, access_token, and access_token_secret from twitter and place it here
  ```
  
const T = new Twit({
  consumer_key: '',
  consumer_secret: '',
  access_token: '',
  access_token_secret: ''
});
```

  4. To start bot type "node index.js" in terminal
  
   
   This 'bot' compares the ticker names of altcoins in the exported array from the names.js file in the tweets its sent. You should probably trim it down and get rid of all the mid tier + super bad ones as a necessary precaution.
   

The buyAmount (on line 13). Is the BTC value of the coin you want to purchase. If your buyAmount is greater than the balance of BTC you have on Poloniex it will not purchase so be careful.

  SafeCheck checks to make sure it is actually his tweet of the day and not some random tweet about another altcoin. I recommend to use it however you may miss something by using it. Its a gamble just like investing in crypto.
