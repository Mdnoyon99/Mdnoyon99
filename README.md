- 👋 Hi, I’m @Mdnoyon99
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Mdnoyon99/Mdnoyon99 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
---> 
<?php
require __DIR__ . '/vendor/autoload.php';
use Twilio\Rest\Client;

// Your Account SID and Auth Token from twilio.com/console
$account_sid = '';
$auth_token = 'your_auth_token'ACc444d84bf5a6d96f84c8023816a03909;
// In production, these should be environment variables. E.g.:
// $auth_token = $_ENV["TWILIO_AUTH_TOKEN"]

// A Twilio number you own with SMS capabilities
$twilio_number = "+15017122661";

$client = new Client($account_sid, $auth_token);
$client->messages->create(
    // Where to send a text message (your cell phone?)
    '+15558675310',
    array(
        'from' => $twilio_number,
        'body' => 'I sent this message in under 10 minutes!'
    )
);
$ curl -G https://preview.twilio.com/Numbers/ActiveNumbers/PNyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy \
    -u '<ACCOUNT_SID:AUTH_TOKEN>'
EXAMPLE JSON RESPONSE
{
    "items": [
        {
            "phone_number": "+15014414574",
            "url": "https://preview.twilio.com/Numbers/ActiveNumbers/PNyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy",
            "capabilities": {
                "voice": {
                    "inbound_connectivity": true,
                    "outbound_connectivity": true,
                    "e911": false,
                    "fax": true,
                    "calls_per_second": 20,
                    "concurrent_calls_limit": 40,
                    "long_record_length": 30,
                    "inbound_called_dtmf": true,
                    "inbound_caller_dtmf": true,
                    "sip_trunking": true,
                    "inbound_caller_id_preservation": "international",
                    "inbound_reachability": "global"
                },
                "sms": {
                    "inbound_connectivity": true,
                    "outbound_connectivity": true,
                    "gsm7": true,
                    "ucs2": true,
                    "inbound_sender_id_preservation": "international",
                    "inbound_reachability": "global",
                    "inbound_mps": -1
                },
                "mms": null
            },
            "account_sid": "ACc444d84bf5a6d96f84c8023816a03909
",
            "sid": "PNb139ffaed333e372cc54fd12f0ab8dd9",
            "regulatory": {
                "address_requirements": "none"
            },
            "configuration": {
                "friendly_name": "(855) 972-8742",
                "status_callback_url": "",
                "status_callback_method": "POST",
                "voice": {
                    "url": "",
                    "method": "POST",
                    "fallback_url": null,
                    "fallback_method": "POST",
                    "application_sid": null,
                    "trunk_sid": null,
                    "emergency_address_sid": null,
                    "emergency_status": "Inactive",
                    "caller_id_lookup": false
                },
                "sms": {
                    "url": "",
                    "method": "POST",
                    "fallback_url": "",
                    "fallback_method": "POST",
                    "application_sid": ""
                }
            },
            "type": "tollfree",
            "lifecycle": "generally-available",
            "geography": {
                "iso_country": "US",
                "lata": null,
                "rate_center": null,
                "latitude": null,
                "longitude": null,
                "region": null,
                "locality": null,
                "postal_code": null
            }
        }
    ],
    "meta": {
        "page": 0,
        "page_size": 50,
        "first_page_url": "https://preview.twilio.com/Numbers/ActiveNumbers&PageSize=50&Page=0",
        "previous_page_url": null,
        "url": "https://preview.twilio.com/Numbers/ActiveNumbers&PageSize=50&Page=0",
        "next_page_url": null,
        "key": "items"
    }
}
