# HashCharger Modal Widget

HashCharger can be integrated into any webpage as a Javscript widget and allows users to purchase hashing power from WariHash's spot market. We are currently in invite-only alpha stage for early adopters. Contact support@warihash.com if you would like to try out HashCharger.

Demo link: https://warihash.com/hashcharger-for-mining-pools/

## Release Notes

[1.0.0](https://github.com/warigroup/hashcharger/releases/tag/1.0.0) : First alpha release. You will not able to set/collect fees yet, this will be in an upcoming release 

[1.0.3](https://github.com/warigroup/hashcharger/releases/tag/1.0.3) : Minor bug fix to prevent modal from being opened multiple times.

## Installation guide

1. If you haven't done so already, register an account at https://market.warihash.com/register. Contact support@warihash.com and we'll give you a unique token that will be used to set up hashcharger with your account.

1. Create a new button with 'open-hashcharger' class on your website. This button will be used to open HashCharger modal window. 

```
<button class="open-hashcharger">Example Button</button>
```

2. Add below script before closing body tag of your html file, change configurations as defined in the next section.

```
<script defer 
  src="https://cdn.jsdelivr.net/gh/warigroup/hashcharger@1.0.3/hashcharger.js"
  id="hashcharger"
  token="FRxtvCGmNWV9AqJRKAs7CB"
  subuser="your_subuser_id"
  stratum-host="stratum.slushpool.com" 
  stratum-port="3333"
  stratum-username="widgetaccount"
  stratum-password="password"
  algorithm="sha256d"
  theme-navbg="3626a5"
  theme-navtexts="ffffff"
  theme-primary="3626a5"
  theme-secondary="233f5c"
  theme-buttontexts="ffffff"
  theme-tabletexts="ffffff">
</script>
```

If you're using React, you can add our script using below method: 

```
  componentDidMount() {
    const script = document.createElement("script");
    script.src = "https://cdn.jsdelivr.net/gh/warigroup/hashcharger@1.0.3/hashcharger.js";
    script.id = 'hashcharger';
    script.setAttribute('token', 'a46KwFe23rgtrgaAfrggWo');
    script.setAttribute('subuser', `${subuser}`)
    script.setAttribute('stratum-host', `${hostaddress}`);
    script.setAttribute('stratum-port', `${port}`);
    script.setAttribute('stratum-username', `${username}`); 
    script.setAttribute('stratum-password', `${password}`);
    script.setAttribute('algorithm', 'equihash-zcash');
    script.setAttribute('theme-navbg', "3626a5");
    script.setAttribute('theme-navtexts', "ffffff");
    script.setAttribute('theme-primary', "3626a5");
    script.setAttribute('theme-secondary', "233f5c");
    script.setAttribute('theme-buttontexts', "ffffff");
    script.setAttribute('theme-tabletexts', "ffffff");
    document.body.appendChild(script);
  }
  
  componentWillUnmount() {
    const script = document.getElementById('hashcharger');
    document.body.removeChild(script);
  }

```
Please use setAttribute() to add attributes to script tag. 
https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute


## Configurations

#### src
Where you will fetch the hashcharger javascript library, should be set to https://cdn.jsdelivr.net/gh/warigroup/hashcharger@1.0.3/hashcharger.js unless you want to serve this file from your own servers.

If you want to serve the js file from your own server, please make sure to include hashcharger.js file in a correct path.

```
<script defer 
  src="/path/to/your/hashcharger.js"
```

#### id 
Don't change this id parameter. id should be set to "hashcharger"

#### token
Unique token value for authorization that we will give you. This identifies who you are to WariHash.

#### subuser
The subuser value identifies who this user is. By using a unique identifier per user (it can be any string, such as an Id, username, or email), each user will be able to retrieve their own orders in the order history page of HashCharger. In addition, the HashCharger integrator will be able to tell which of their user bought hashing power by the subuser value. 

#### stratum-host
Stratum host where hashing power will be directed to (i.e, stratum.slushpool.com)

#### stratum-port
Port number where hashing power will be directed to 

#### stratum-username
Stratum username that hashing power will be direted to

#### stratum-password
Stratum password that hashing power wil be directed to

#### algorithm
Algorithm to purchase hashing power for (currently available: sha256d, scrypt, handshake, ethash, equihash-zcash)

## Theme color hex codes 

#### !! Warning: don't include # in hex code. 
#### Colors must use six digit hex code values. Parameters can't use color names. i.e. violet, purple, cyan, etc.

#### theme-navbg
Bottom navigation background color hex code

#### theme-navtexts
Bottom navigation text color hex code

#### theme-primary
Primary theme color on the main page hex code

#### theme-secondary
Secondary theme color on order history page hex code

#### theme-buttontexts
Button text color hex code

#### theme-tabletexts
Table menu text color hex code
