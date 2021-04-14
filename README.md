# geoDetailsJavscriptApi
With This code you will get user location details vai api.. 

ipgeolocation
https://ipgeolocation.io/

Limitations:

    50,000 requests per month
    Requires registration to get your API key
    Returns only IPv6 address if you have that


---------------------------------------------------------------
Geobytes

Try it: http://gd.geobytes.com/GetCityDetails

$.getJSON('http://gd.geobytes.com/GetCityDetails?callback=?', function(data) {
  console.log(JSON.stringify(data, null, 2));
});


Returns:

{
  "geobytesforwarderfor": "",
  "geobytesremoteip": "116.12.250.1",
  "geobytesipaddress": "116.12.250.1",
  "geobytescertainty": "99",
  "geobytesinternet": "SA",
  "geobytescountry": "Saudi Arabia",
  "geobytesregionlocationcode": "SASH",
  "geobytesregion": "Ash Sharqiyah",
  "geobytescode": "SH",
  "geobyteslocationcode": "SASHJUBA",
  "geobytescity": "Jubail",
  "geobytescityid": "13793",
  "geobytesfqcn": "Jubail, SH, Saudi Arabia",
  "geobyteslatitude": "27.004999",
  "geobyteslongitude": "49.660999",
  "geobytescapital": "Riyadh ",
  "geobytestimezone": "+03:00",
  "geobytesnationalitysingular": "Saudi Arabian ",
  "geobytespopulation": "22757092",
  "geobytesnationalityplural": "Saudis",
  "geobytesmapreference": "Middle East ",
  "geobytescurrency": "Saudi Riyal",
  "geobytescurrencycode": "SAR",
  "geobytestitle": "Saudi Arabia"
}

Limitations:

    16,384 requests per hour
    No SSL (https) with the free plan
    Can return the wrong location
---------------------------------------------------




I would use a web service that can return JSON (along with jQuery to make things simpler). Below are all the active free IP lookup services I could find and the information they return. If you know of others, then please add a comment and I'll update this answer.
Abstract

let apiKey = '1be9a6884abd4c3ea143b59ca317c6b2';
$.getJSON('https://ipgeolocation.abstractapi.com/v1/?api_key=' + apiKey, function(data) {
  console.log(JSON.stringify(data, null, 2));
});

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>

Full page

Limitations:

    10,000 requests per month
    Requires registration to get your API key

BigDataCloud

// Base
let apiKey = 'd9e53816d07345139c58d0ea733e3870';
$.getJSON('https://api.bigdatacloud.net/data/ip-geolocation?key=' + apiKey, function(data) {
  console.log(JSON.stringify(data, null, 2));
});

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>

Full page

// Base + Confidence Area
let apiKey = 'd9e53816d07345139c58d0ea733e3870';
$.getJSON('https://api.bigdatacloud.net/data/ip-geolocation-with-confidence?key=' + apiKey, function(data) {
  console.log(JSON.stringify(data, null, 2));
});

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>

Expand snippet

// Base + Confidence Area + Hazard Report
let apiKey = 'd9e53816d07345139c58d0ea733e3870';
$.getJSON('https://api.bigdatacloud.net/data/ip-geolocation-full?key=' + apiKey, function(data) {
  console.log(JSON.stringify(data, null, 2));
});

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>

Expand snippet

Limitations:

    10,000 requests per month
    Requires registration to get your API key

Cloudflare

$.get('https://www.cloudflare.com/cdn-cgi/trace', function(data) {
  // Convert key-value pairs to JSON
  // https://stackoverflow.com/a/39284735/452587
  data = data.trim().split('\n').reduce(function(obj, pair) {
    pair = pair.split('=');
    return obj[pair[0]] = pair[1], obj;
  }, {});
  console.log(data);
});

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>

Expand snippet

Limitations:

    Returns plain text
    Returns only IPv6 address if you have that

DB-IP

Try it: https://api.db-ip.com/v2/free/self

$.getJSON('https://api.db-ip.com/v2/free/self', function(data) {
  console.log(JSON.stringify(data, null, 2));
});

Returns:

{
  "ipAddress": "116.12.250.1",
  "continentCode": "AS",
  "continentName": "Asia",
  "countryCode": "SG",
  "countryName": "Singapore",
  "city": "Singapore (Queenstown Estate)"
}

Limitations:

    1,000 requests per day
    Requires non-null Origin request header

Geobytes

Try it: http://gd.geobytes.com/GetCityDetails

$.getJSON('http://gd.geobytes.com/GetCityDetails?callback=?', function(data) {
  console.log(JSON.stringify(data, null, 2));
});

Returns:

{
  "geobytesforwarderfor": "",
  "geobytesremoteip": "116.12.250.1",
  "geobytesipaddress": "116.12.250.1",
  "geobytescertainty": "99",
  "geobytesinternet": "SA",
  "geobytescountry": "Saudi Arabia",
  "geobytesregionlocationcode": "SASH",
  "geobytesregion": "Ash Sharqiyah",
  "geobytescode": "SH",
  "geobyteslocationcode": "SASHJUBA",
  "geobytescity": "Jubail",
  "geobytescityid": "13793",
  "geobytesfqcn": "Jubail, SH, Saudi Arabia",
  "geobyteslatitude": "27.004999",
  "geobyteslongitude": "49.660999",
  "geobytescapital": "Riyadh ",
  "geobytestimezone": "+03:00",
  "geobytesnationalitysingular": "Saudi Arabian ",
  "geobytespopulation": "22757092",
  "geobytesnationalityplural": "Saudis",
  "geobytesmapreference": "Middle East ",
  "geobytescurrency": "Saudi Riyal",
  "geobytescurrencycode": "SAR",
  "geobytestitle": "Saudi Arabia"
}

Limitations:

    16,384 requests per hour
    No SSL (https) with the free plan
    Can return the wrong location

GeoIPLookup.io
https://geoiplookup.io/api

$.getJSON('https://json.geoiplookup.io/?callback=?', function(data) {
  console.log(JSON.stringify(data, null, 2));
});

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>

Expand snippet

Limitations:

    10,000 requests per hour
    Free plan only for non-commercial use
    Returns only IPv6 address if you have that
