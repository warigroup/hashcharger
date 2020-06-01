## Installation guide for Angular frontend

If you're using Angular 2+, you can add our script using below method: 

```
  ngOnInit() { 
    const script = document.createElement('script');
    script.src = 'https://cdn.jsdelivr.net/gh/warigroup/hashcharger@1.0.3/hashcharger.js';
    script.id = 'hashcharger';
    script.setAttribute('token', 'a46KwFe23rgtrgaAfrggWo');
    // pass in your dynamic subuser and stratum config here.
    script.setAttribute('subuser', `${subuser}`);
    script.setAttribute('stratum-host', `${hostaddress}`);
    script.setAttribute('stratum-port', `${port}`);
    script.setAttribute('stratum-username', `${username}`);
    script.setAttribute('stratum-password', `${password}`);
    script.setAttribute('algorithm', 'equihash-zcash');
    script.setAttribute('theme-navbg', '3626a5');
    script.setAttribute('theme-navtexts', 'ffffff');
    script.setAttribute('theme-primary', '3626a5');
    script.setAttribute('theme-secondary', '233f5c');
    script.setAttribute('theme-buttontexts', 'ffffff');
    script.setAttribute('theme-tabletexts', 'ffffff');
    document.body.appendChild(script);
   }

  ngOnDestroy() {
    const script = document.getElementById('hashcharger');
    document.body.removeChild(script);
  }

```
Please use setAttribute() to add attributes to script tag. 
https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute
