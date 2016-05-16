Adapted from https://github.com/jw84/messenger-bot-tutorial
# Creating your own FB chatbot with KooKoo

![Alt text](/demo/Demo.gif)

Facebook recently opened up their Messenger platform to enable bots to converse with users through Facebook Apps and on Facebook Pages. 

You can read the  [documentation](https://developers.facebook.com/docs/messenger-platform/quickstart) the Messenger team prepared but it's not very clear for beginners and intermediate hackers. 

## 🙌 Get set

Messenger bots uses a web server to process messages it receives or to figure out what messages to send. You also need to have the bot be authenticated to speak with the web server and the bot approved by Facebook to speak with the public.

### *Setup the Facebook App*

1. Create or configure a Facebook App or Page here https://developers.facebook.com/apps/

    ![Alt text](/demo/step1.png)

2. In the app go to Messenger tab then click Setup Webhook. Here you will put in the URL of our KooKoo server ( https://kookoo.in/customers/fb_webhook/app.php) and a verify token ( kookoo_is_the_best ). Make sure to check all the subscription fields. 

    ![Alt text](/demo/step2.png)
    
    ![Alt text](/demo/step3.png)

3. Once you setup the webhook it should show complete in green color ,Now Link the FB app to your page. Select Facebook Page and Get a Page Access Token and save this somewhere. 

    ![Alt text](/demo/step4.png)

4. Go back to Terminal and type in this command to trigger the Facebbook app to send messages. Remember to use the token you requested earlier.

    ```
    curl -X POST "https://graph.facebook.com/v2.6/me/subscribed_apps?access_token=<PAGE_ACCESS_TOKEN>"
     
    If successful, you will receive a response:
    {
      "success": true
    }
    ```
5. Share the URL which is hosted publicly at your end with sample php code given below, which will be configured on our KooKoo Platform to recieve the events from your page to the URL. Once you do this you are ready with your basic working chatbot. 

For building complex chatbot mail us to the below email id.

    ```
     <?php
        echo "<response><chat-reply>Hi,I am a messenger bot.To get more, say more or next. 
        Or say bye to close me.</chat-reply></response>";

     ?>
    ```
## How I can help

Email us for help! support@kookoo.in.
