To reproduce
```
Darwin dev-team.local 21.4.0 Darwin Kernel Version 21.4.0: Fri Mar 18 00:45:05 PDT 2022; root:xnu-8020.101.4~15/RELEASE_X86_64 x86_64
npx create-next-app@latest --js --use-yarn
Add server code following https://nextjs.org/docs/pages/building-your-application/configuring/custom-server
```

```bash
yarn dev
```

The error
```baash
$ node server.js
> Ready on http://localhost:3000
- event compiled client and server successfully in 345 ms (20 modules)
- wait compiling...
- event compiled client and server successfully in 164 ms (20 modules)
Error: connect ECONNREFUSED ::1:60481
    at TCPConnectWrap.afterConnect [as oncomplete] (node:net:1494:16) {
  errno: -61,
  code: 'ECONNREFUSED',
  syscall: 'connect',
  address: '::1',
  port: 60481
}
```
Note that the 60481 port is actually random. It will change on next start.