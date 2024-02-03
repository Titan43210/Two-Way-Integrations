# Two-Way-Integrations
This project demonstrates the implementation of a two-way integration system that synchronizes a local customer catalog with an external service, specifically Stripe, in near real-time. The integration is designed to be extendable for future integrations with other catalogs and systems within the product.

Running it locally
Clone the respository using HTTPS or SSH method.
Create a virtual environment. Use this link as reference.
Activate the environment according to the OS you are currenlty using.
Install all the dependencies needed to run this project using pip install -r requirements.txt
Create a stripe test account and paste the API_KEY provided to you in .env file with key 'STRIPE_API_KEY' by creating it in parent directory.
Now open 3 terminals in the parent directory of this project:
To run the main.py file using the command uvicorn main:app --reload
To run the server.py to store the messages in queue using python server.py
To expose our local server to the Stripe or Internet using ngrok http 8000 as 8000 is the PORT we are using to run our main.py
The 3rd terminal provides us a random URL similar to https://1b81-117-219-22-193.ngrok-free.app which we need to add in Stripe as webhook hosted endpoint. Make sure that you add /stripe-webhook at the end of URL so that it becomes a correct endpoint.
You are all set to play with this project now.
