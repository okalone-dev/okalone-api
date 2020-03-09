# okalone-api -- update 1.1

Lone worker REST API integration, ok alone

Integrating your application with Ok Alone starts with using the API calls. Most integrations use the primary Ok Alone features such as Check-in, Start shift, End shit and Man down / Call for help.

Here's a list of the Ok Alone API and how to use them:

Add location for this worker
POST 
/location/add

Example Body:
{
"location": {
"lat": 54.3266022,
"lng": -2.776066,
"source":"gps",
"accuracy":10
 }
}


Checkin worker to let okalone know your worker is safe:
POST 
/status/ok

Example Body:
{
"location": {
"lat": 54.3266022,
"lng": -2.776066,
"source":"gps",
"accuracy":10
 }
}


End shift when your workers day is done:
POST
/status/end

Example Body:
{
"location": {
"lat": 54.3266022,
"lng": -2.776066,
"source":"gps",
“accuracy":10
 }
}


Send help if the worker is having a problem
POST
/status/help

{
"location": {
"lat": 54.3266022,
"lng": -2.776066,
"source":"gps",
"accuracy":10
 }
}

Receive shift information for the worker
POST
/status/info



Learn more about the Ok Alone Lone worker saftey solution at: https://okaloneworker.com/

