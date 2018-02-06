# internal-ip

> Get your internal IP address

It forks from [Sindre Sorhus](https://github.com/sindresorhus/internal-ip), for hide popup window run with pm2 on windows.

## Install

```
$ npm install @penggy/internal-ip
```


## Usage

```js
const internalIp = require('@penggy/internal-ip');

internalIp.v6().then(ip => {
	console.log(ip);
	//=> 'fe80::1'
});

internalIp.v4().then(ip => {
	console.log(ip);
	//=> '10.0.0.79'
});

console.log(internalIp.v6.sync())
//=> 'fe80::1'

console.log(internalIp.v4.sync())
//=> '10.0.0.79'
```

The module returns the address of the internet-facing interface, as determined from the default gateway. When the address cannot be determined for any reason, `null` will be returned.

The module relies on operating systems tools. On Linux and Android, the `ip` command must be available, which depending on distribution might not be installed by default. It is usually provided by the `iproute2` package.


## Related

- [internal-ip-cli](https://github.com/sindresorhus/internal-ip-cli) - CLI for this module
- [public-ip](https://github.com/sindresorhus/public-ip) - Get your public IP address
- [default-gateway](https://github.com/silverwind/default-gateway) - Get your default gateway address


## License

MIT © [Sindre Sorhus](https://sindresorhus.com)
