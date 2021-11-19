# Debugging

## Breakpoints

Are you tired of having to rely on `console.log()` to debug your code?
This document will show you how to setup breakpoints in VSCode and WebStorm to help you with debugging.

1. Start the server.
```bash
make dev
```

2. Configure IDE debugging:

### VSCode

a. Click on "Run and Debug" in the left hand side of vscode and click on the green play button.
![image](https://i.imgur.com/Sn5vd6l.png)
b. Open a file like `SocketServer.ts` and add breakpoints.
![image](https://i.imgur.com/GooSLfE.png)
c. Go to https://localhost:8080 and use the site like normal. When the server reaches the breakpoints you've set, it will stop running and you will be able to examine all the variables defined in the scope.
![image](https://i.imgur.com/Z8w2CgV.png)
d. Hit the forward button when you want the server to continue running.
![image](https://i.imgur.com/kukJYRX.png)
   
### WebStorm

a. Open `Run/Debug Configurations` (`Run->Edit Configurations`)
b. Add a new configuration for `Attach to Node.js/Chrome`.
![image](https://i.imgur.com/oAe5gsv.png)
c. Place your breakpoints accordingly
![image](https://i.imgur.com/M4FoVpF.png)
d. When the breakpoint is triggered, the execution will stop. You now have full control over everything you need such as the stack trace and watchlist.
![image](https://i.imgur.com/MzTtyVv.png)

## Prevent game from timing out

If you are debugging a running game, the game will time out after 1 minute by default. If you need more time to debug a running game you can modify `GameController.abandonedGameShutDownTimeout` to increase the game timeout.

Example:

```ts
static readonly abandonedGameShutDownTimeout = 1000 * 60 * 60 * 24 // Milliseconds
```

## Debugging Pixi.js / Canvas

It is possible to inspect elements in the game canvas.

1. You will need to install the PIXI inspector Chrome extension: 
   https://github.com/bfanger/pixi-inspector
2. After installing, open `Chrome Developer Tools`, then open the `Pixi` tab.
3. The scene graph should now be visible.
   You can edit attributes for individual objects.
   Selected objects will also be highlighted.
   ![image](https://i.imgur.com/i8oi6Uq.png)
