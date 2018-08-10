# HelpCard

<b>Context/Feature</b>: Customers often ask the same questions to customer service agent, which can be easily answered without direct contacting. In order to make the customer service better and more to streamline operations, we'll introduce the Help section. The main part of the help section will be the so-called info cards. Every card contains information that is relevant for the user. For the sake of this task we implement cards which each represent an order. Each card is tappable and a tap would lead to a different screen which uses the order_id to display more help information.



<b>Task:</b>
1. Implement the view by creating a simple empty Android application. Try to be as accurate as possible with the UI implementation.

2. Stub a transition to a not yet implemented order detail screen 

3. The endpoint ORDERS provides orders that are interesting to the user, implement code to call the API and make use of the data 

4. Our REST API returns the orders unsorted! For legacy reasons this cannot be changed - please sort the returned orders by arrives_at_utc. 

5. Long time customers might see a lot of orders. Help our UX designer! She did not find a good method yet for displaying the current position. Also consider performance by using an appropriate adapter.

ORDERS endpoint (returns new random data for each call) 

<b>GET</b> http://staging-api.xxx.com/test/orders

<b>200 OK</b> Response Body: 
```
{  
   “orders”:[
      {
         “order_id”:numeric,
         // UNIX time,
         milliseconds since 1970 - convert to local time! “arrives_at_utc”:numeric,
         “paid_with”:string
      }
      
   ]
}

```
<b><i>output</i></b>
503 Service unavailable
Oh no! What happened? :( Make sure the App can handle this temporary error response gracefully.
