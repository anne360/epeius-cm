# epeius
This is a script based on the CF Worker platform. It modifies the original version to display Trojan configuration information and convert it into subscription content. Using this script, you can easily convert Trojan configuration information to tools such as Clash or Singbox using online configuration.

- **One-step deployment** video tutorial: https://youtu.be/MBlAqYajVSY ***A must-see for beginners, one-step to the stomach, best recommendation!!!***
- **Self-made preferred** subscription video tutorial: https://youtu.be/jOhq3QpXG_I *Toss your own exclusive subscription*
- **Advanced use** skills video tutorial: https://youtu.be/0Cd8uTNJj1Q *Then become the king of tossing*

Telegram communication group: [@CMLiussss](https://t.me/CMLiussss), **Thanks to [Alice Networks](https://url.cmliussss.com/alice) for providing cloud servers to maintain [CM subscription conversion service](https://sub.fxxk.dedyn.io/)! **

# Disclaimer

This disclaimer applies to the "epeius" project on GitHub (hereinafter referred to as "this project"), the project link is: https://github.com/cmliu/epeius .

### Purpose
This project is designed and developed for educational, research and security testing purposes only. It aims to provide a tool for security researchers, academics and technology enthusiasts to explore and practice network communication technology.

### Legality
When downloading and using the code of this project, you must comply with the laws and regulations applicable to the user. It is the responsibility of the user to ensure that his or her behavior complies with the legal framework, rules and regulations and other relevant regulations of the region in which he or she is located.

### Disclaimer
1. As the **secondary development author** of this project (hereinafter referred to as the "author"), I **cmliu** emphasize that this project should only be used for legal, ethical and educational purposes.
2. The author does not approve, support or encourage any form of illegal use. If it is found that this project is used for any illegal or unethical activities, the author will strongly condemn it.
3. The author is not responsible for any illegal activities carried out by any person or organization using the code of this project. Any consequences arising from the use of the code of this project shall be borne by the user.
4. The author is not responsible for any direct or indirect damage that may be caused by the use of the code of this project.
5. To avoid any unexpected consequences or legal risks, users should delete the code within 24 hours after using the code of this project.

By using the code of this project, users understand and agree to all the terms of this disclaimer. If users do not agree to these terms, they should stop using this project immediately.

The author reserves the right to update this disclaimer at any time without further notice. The latest version of the disclaimer will be published on the GitHub page of this project.

## Risk Warning
- Avoid node configuration information leakage by submitting false node configuration to the subscription service.
- In addition, you can also choose to deploy [WorkerVless2sub Subscription Generation Service](https://github.com/cmliu/WorkerVless2sub) by yourself, so that you can take advantage of the convenience of the subscription generator.

## Workers Deployment Method [Video Tutorial](https://www.youtube.com/watch?v=MBlAqYajVSY&t=169s)
1. Deploy CF Worker:
- Create a new Worker in the CF Worker console.
- Paste the contents of [worker.js](https://github.com/cmliu/epeius/blob/main/_worker.js) into the Worker editor.
- Change the third line `password` to your own **password**

2. Add preferred lines:

- Add preferred domain names/preferred IPs to `addresses` in the format. If the port number is not included, the default TLS port is 443. The # sign is followed by a remark alias, for example:
```js
let addresses = [
// Enable local preferred domain names/preferred IPs when sub is empty
'www.visa.com.sg#Official preferred domain name',
'www.wto.org:8443#Official preferred domain name',
'visa.cn:2087',
'icook.hk',
];
```
- Or add the **Trojan preferred subscription generator** address to `sub`, for example:
```js
let sub = 'Trojan.fxxk.dedyn.io';
```

3. Access subscription content:
- Access `https://[YOUR-WORKERS-URL]/[PASSWORD]` to get the subscription content.
- For example, `https://vless.google.workers.dev/auto` is your universal adaptive subscription address.
- For example, `https://vless.google.workers.dev/auto?sub` Base64 subscription format, suitable for PassWall, SSR+, etc.
- For example, `https://vless.google.workers.dev/auto?clash` Clash subscription format, suitable for OpenClash, etc.
- For example, `https://vless.google.workers.dev/auto?sb` singbox subscription format, suitable for singbox, etc.

4. Bind custom domains to workers:
- In the `Triggers` tab of the workers console, click `Add custom domain` at the bottom.
- Fill in the secondary domain name you have transferred to the CF domain name resolution service, for example: `vless.google.com`, then click `Add custom domain` and wait for the certificate to take effect.

## Pages upload deployment method
1. Deploy CF Pages:
- Download the [main.zip](https://github.com/cmliu/epeius/archive/refs/heads/main.zip) file and click Star!!!
- After selecting `Upload assets` in the CF Pages console, name your project and click `Create project`, then upload the downloaded [main.zip](https://github.com/cmliu/epeius/archive/refs/heads/main.zip) file and click `Deploy site`.
- After the deployment is complete, click `Continue processing site`, select `Settings` > `Environment variables` > **Make** define variables for production environment > `Add variables`.
Fill in **PASSWORD** for the variable name, and the value is your password, then click `Save`.
- Return to the `Deployment` tab, click `Create New Deployment` in the lower right corner, re-upload the [main.zip](https://github.com/cmliu/epeius/archive/refs/heads/main.zip) file, and click `Save and Deploy`.

2. Add preferred routes:
- Add variable `ADD` Local static preferred routes, if no port number is included, the default TLS port is 443, and the # sign is followed by a remark alias, for example:
```
12315.cf.090227.xyz:443#Join my channel t.me/CMLiussss to unlock more preferred nodes
visa.cn#You can only put the domain name as follows
www.visa.com.sg
time.is#You can also put the domain name with the port as follows
www.wto.org:8443
chatgpt.com:2087#The node name can be placed after the # sign
icook.hk#If no port number is included, the default port is 443
104.17.152.41#IP is also OK
[2606:4700:e7:25:4b9:f8f8:9bfb:774a]#IPv6 is also OK
```

3. Access subscription content:
- Visit `https://[YOUR-PAGES-URL]/[PASSWORD]` to get subscription content.
- For example, `https://epeius.pages.dev/auto` is your universal adaptive subscription address.
- For example, `https://epeius.pages.dev/auto?sub` Base64 subscription format, suitable for PassWall, SSR+, etc.
- For example, `https://epeius.pages.dev/auto?clash` Clash subscription format, suitable for OpenClash, etc.
- For example, `https://epeius.pages.dev/auto?sb` singbox subscription format, suitable for singbox, etc.
- For example, `https://epeius.pages.dev/auto?surge` surge subscription format, suitable for surge 4/5.

4. Bind CNAME custom domain to Pages:
- In the `Custom Domains` tab of the Pages console, click `Set Custom Domain` below.
- Fill in your custom subdomain name, be careful not to use your root domain name, for example:
If the domain name you are assigned is `fuck.cloudns.biz`, then add a custom domain and fill in `lizi.fuck.cloudns.biz`;
- According to CF's requirements, your domain name DNS service provider will be returned. After adding the CNAME record `epeius.pages.dev` of the custom domain `lizi`, click `Activate Domain`.

## Pages GitHub Deployment Method [Video Tutorial](https://www.youtube.com/watch?v=0Cd8uTNJj1Q&t=96s)
1. Deploy CF Pages:
- Fork this project on Github first and click Star!!!
- After selecting `Connect to Git` in the CF Pages console, select the `epeius` project and click `Start Setting`.
- Under the `Set up build and deployment` page, select `Environment variables (advanced)` and click `Add variable`.
Fill in **PASSWORD** as the variable name and your password as the value. Then click `Save and deploy`.

2. Add preferred routes:
- Add variable `ADD` Local static preferred routes, if no port number is included, the default TLS port is 443, and the # sign is followed by a remark alias, for example:
```
12315.cf.090227.xyz:443#Join my channel t.me/CMLiussss to unlock more preferred nodes
visa.cn#You can only put the domain name as follows
www.visa.com.sg
time.is#You can also put the domain name with the port as follows
www.wto.org:8443
chatgpt.com:2087#The node name can be placed after the # sign
icook.hk#If no port number is included, the default port is 443
104.17.152.41#IP is also OK
[2606:4700:e7:25:4b9:f8f8:9bfb:774a]#IPv6 is also OK
```

3. Access subscription content:
- Visit `https://[YOUR-PAGES-URL]/[PASSWORD]` to get subscription content.
- For example, `https://epeius.pages.dev/auto` is your universal adaptive subscription address.
- For example, `https://epeius.pages.dev/auto?sub` Base64 subscription format, suitable for PassWall, SSR+, etc.
- For example, `https://epeius.pages.dev/auto?clash` Clash subscription format, suitable for OpenClash, etc.
- For example, `https://epeius.pages.dev/auto?sb` singbox subscription format, suitable for singbox, etc.
- For example, `https://epeius.pages.dev/auto?surge` surge subscription format, suitable for surge 4/5.

4. Bind CNAME custom domain to Pages:
- In the `Custom Domains` tab of the Pages console, click `Set Custom Domain` at the bottom.
- Fill in your custom secondaryDomain name, be careful not to use your root domain name, for example:
If the domain name you are assigned is `fuck.cloudns.biz`, then add a custom domain and fill in `lizi.fuck.cloudns.biz`;
- According to CF's requirements, your domain name DNS service provider will be returned. After adding the CNAME record `epeius.pages.dev` of the custom domain `lizi`, click `Activate Domain`.

## Variable description
| Variable name | Example | Remarks |
|--------|---------|-----|
| PASSWORD | `auto` | Can take any value |
| PROXYIP | `proxyip.fxxk.dedyn.io:443` | Alternative proxy node for accessing CFCDN sites (supports multiple ProxyIPs, use `,` or `newline` as a separator between ProxyIPs) |
| SOCKS5 | `user:password@127.0.0.1:1080` | Prioritize as a SOCKS5 proxy for accessing CFCDN sites (supports multiple socks5s, use `,` or `newline` as a separator between socks5s) |
| GO2SOCKS5 | `blog.cmliussss.com`,`*.ip111.cn`,`*google.com` | After setting the `SOCKS5` variable, you can force the use of socks5 access list (`*` can be used as a wildcard, `newline` can be used to separate multiple elements) |
| ADD | `www.csgo.com:2087,icook.hk` | Local preferred domain name/preferred IP (supports `,` or `newline` between multiple elements as separators) |
| ADDAPI | [https://raw.github.../addressesapi.txt](https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressesapi.txt) | No explanation, those who understand will understand |
| ADDCSV | [https://raw.github.../addressescsv.csv](https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressescsv.csv) | No explanation, those who understand will understand |
| DLS | `8` | `ADDCSV` speed test results meet the lower speed limit |
| TGTOKEN | `6894123456:XXXXXXXXXX0qExVsBPUhHDAbXXXXXqWXgBA` | Robot token for sending TG notifications |
| TGID | `6946912345` | Account digital ID for receiving TG notifications |
| SUB | `Trojan.fxxk.dedyn.io` | Preferred subscription generator address (using the subscriber will abandon the local preferred subscription content in `ADD`) |
| SUBAPI | `SUBAPI.fxxk.dedyn.io` | Subscription conversion backend such as clash and singbox |
| SUBCONFIG | [https://raw.github.../ACL4SSR_Online_Mini.ini](https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/config/ACL4SSR_Online_Mini.ini) | Subscription conversion configuration file such as clash and singbox |
| SUBNAME | `epeius` | Subscription name |
| RPROXYIP | `false` | Set to true to force the acquisition of the ProxyIP assigned by the subscriber (subscriber support required) |
| URL302 | `https://t.me/CMLiussss` | Home page 302 jump (supports multiple URLs, use `,` or `newline` as a separator between URLs, don't use it if you're new to this) |
| URL | `https://blog.cmliussss.com` | Home page anti-genuine camouflage (supports multiple URLs, use `,` or `newline` as a separator between URLs, random settings can easily trigger anti-fraud) |
| CFEMAIL | `admin@gmail.com` | CF account email (after filling in `CFKEY`, the subscription information will display the request usage, don't use it if you're new to this) |
| CFKEY | `c6a944b5c956b6c18c2352880952bced8b85e` | CF account Global API Key (After filling in both `CFEMAIL`, the subscription information will display the request usage, so don't use it if you are new to it) |
| CFPORTS | `2053`,`2096`,`8443` | CF account standard port list |

**Note: After filling in `SOCKS5`, `PROXYIP` will no longer be enabled! Please choose one of the two! ! ! **

**Note: After filling in `SUB`, the subscription content generated by the `ADD*` class variable will no longer be enabled! Please choose one of the two! ! ! **

**Note: Filling in `CFEMAIL` and `CFKEY` at the same time will enable the display of request usage, but it is not recommended! There is no need to give a Worker project such high permissions! You will be at your own risk! ! ! **

## Practical tips

**The subscription deployed by this project can quickly change the preferred subscription generator by adding the `sub` key value! **
> For example, `https://epeius.pages.dev/auto` is your universal adaptive subscription address
- Quickly change the subscription address of the subscriber to `Trojan.fxxk.dedyn.io`

```url
https://epeius.pages.dev/auto?sub=Trojan.fxxk.dedyn.io
```

**The nodes deployed in this project can use the specified `PROXYIP` or `SOCKS5` through the node PATH (path) method! ! ! **

- Example of specifying `PROXYIP`
```url
/proxyip=proxyip.fxxk.dedyn.io
/?proxyip=proxyip.fxxk.dedyn.io
/proxyip.fxxk.dedyn.io (only for domains starting with 'proxyip.')
```

- Example of specifying `SOCKS5`
```url
/socks5=user:password@127.0.0.1:1080
/?socks5=user:password@127.0.0.1:1080
/socks://dXNlcjpwYXNzd29yZA==@127.0.0.1:1080
/socks5://user:password@127.0.0.1:1080
```

**When your `ADDAPI` can be used as a `PROXYIP`, you can add `?proxyip=true` to the end of the `ADDAPI` variable, and then use the preferred IP itself as the `PROXYIP` when generating nodes**
- Specify `ADDAPI` as a `PROXYIP` example
```url
https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressesapi.txt?proxyip=true
```

## Star Stars Go
[![Stargazers over time](https://starchart.cc/cmliu/epeius.svg?variant=adaptive)](https://starchart.cc/cmliu/epeius)

## Adapted Clients
### Windows
- [v2rayN](https://github.com/2dust/v2rayN)
- clash.meta ([FlClash](https://github.com/chen08209/FlClash), [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev), [Clash Nyanpasu](https://github.com/keiko233/clash-nyanpasu)) ### IOS - Surge, little rocket - sing-box（[SFI](https://sing-box.sagernet.org/zh/clients/apple/)） ### Android - clash.meta ([ClashMetaForAndroid](https://github.com/MetaCubeX/ClashMetaForAndroid), [FlClash](https://github.com/chen08209/FlClash)) - sing-box ([SFA](https://github.com/SagerNet/sing-box)) ### MacOS - clash.meta（[FlClash](https://github.com/chen08209/FlClash)）

# grateful [ca110us](https://github.com/ca110us/epeius), [xream](https://github.com/xream), [3Kmfi6HP](https://github.com/3Kmfi6HP/EDtunnel/tree/trojan), [zizifn](https://github.com/zizifn/edgetunnel), [emn178](https://github.com/emn178/js-sha256), [ACL4SSR](https://github.com/ACL4SSR/ACL4SSR/tree/master/Clash/config), [SHIJS1999](https://github.com/SHIJS1999/cloudflare-worker-vless-ip), <a href="https://url.cmliussss.com/alice"><img src="https://alicenetworks.net/templates/lagom2/assets/img/logo/logo_big.194980063.png" width="150" height="75" alt="Alice Networks LTD"/></a>,
