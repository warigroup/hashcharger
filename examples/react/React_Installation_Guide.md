## Installation guide for React.js frontend

If you're using React, you can add our script using below method: 

```
  componentDidMount() {
    const script = document.createElement("script");
    script.src = "https://cdn.jsdelivr.net/gh/warigroup/hashcharger@1/hashcharger.js";
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
  
  render() {
    return (
      <div>
        <button className="open-hashcharger">my button</button>
      </div>
    )
  }

```
Please use setAttribute() to add attributes to script tag. 
https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute
