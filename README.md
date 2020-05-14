# HashCharger Modal Widget

Hashcharger can be integrated into any webpage as a Javscript widget and allows users to purchase hashing power from WariHash's spot market. 

Demo link: https://devmarket.warihash.org/demo

## Installation guide

1. If you haven't done so already, register an account at https://market.warihash.com/register. Contact support@warihash.com and we'll give you a unique token that will be used to set up hashcharger with your account.

1. Create a new button with 'open-hashcharger' class on your website. This button will be used to open HashCharger modal window. 

```
<button class="open-hashcharger">Example Button</button>
```

2. Add below script before closing body tag of your html file, change configurations as defined in the next section.

```
<script defer 
  src="https://cdn.jsdelivr.net/gh/warigroup/hashcharger@1/hashcharger.js"
  id="hashcharger"
  token="6j5KRGUkhUZfsXMgMATUgb"
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

## Configurations

#### src
where you will fetch the hashcharger javascript library, should be set to https://cdn.jsdelivr.net/gh/warigroup/hashcharger@1/hashcharger.js unless you want to serve this from your own servers.

#### id 
don't change this ID parameter. id should be set to "hashcharger"

#### token
unique token value for authorization that we will give you. This identifies who you are to WariHash.

#### stratum-host
stratum host where hashing power will be directed to

#### stratum-port
port where hashing power will be directed to

#### stratum-username
stratum username that hashing power will be direted to

#### stratum-password
stratum password that hashing power wil be directed to

#### algorithm
algorithm to purchase hashing power for (currently available: sha256d, scrypt, handshake, ethash, equihash-zcash)

#### theme-navbg
#### theme-navtexts
#### theme-primary
#### theme-secondary
#### theme-buttontexts
#### theme-tabletexts
#### fullscreen
