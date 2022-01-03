## Instalation

1. Create a new script called `start.ns` by issuing the following command: `nano start.ns`. Make sure you're on your home server if you're not (you can quickly go home by running `home` in the console).
2. Paste the following content:

```javascript
/** @param {NS} ns **/
export async function main(ns) {
  if (ns.getHostname() !== "home") {
    throw new Exception("Run the script from home");
  }

  await ns.wget(
    `https://raw.githubusercontent.com/Noa3/Bitburner_auto/master/src/initHacking.ns?ts=${new Date().getTime()}`,
    "initHacking.ns"
  );
  ns.spawn("initHacking.ns", 1);
}
```

3. Exit the nano and write in console: `run start.ns`# Bitburner_auto 

## Credits
Credits for the idea goes too https://raw.githubusercontent.com/moriakaice/