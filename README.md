<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=28&duration=3500&pause=1000&color=F40552&center=true&vCenter=true&width=750&lines=FiveM+Anti-Cheat+Specialist;I+Protect+Servers+From+Cheaters;Detect.+Analyze.+Ban." alt="FiveM Anti-Cheat Specialist" />

![FiveM](https://img.shields.io/badge/FiveM-Anti--Cheat-F40552?style=for-the-badge)
![Server](https://img.shields.io/badge/Server-Security-00D4FF?style=for-the-badge)
![Exploit](https://img.shields.io/badge/Exploit-Prevention-2ea44f?style=for-the-badge)
![Moderation](https://img.shields.io/badge/Cheater-Hunting-8A2BE2?style=for-the-badge)

</div>

---

## 🎯 What I Do

I work as an **anti-cheat specialist on FiveM servers**. My job is to find cheaters, stop exploits before they hurt the economy, and keep the game fair for honest players.

## 🔍 Cheats & Exploits I Deal With

| Category | Examples |
|---|---|
| 🎯 **Combat Cheats** | Aimbot, triggerbot, silent aim, no recoil, rapid fire |
| 👻 **Movement Cheats** | Noclip, godmode, speedhack, teleport, fly, super jump |
| 💉 **Mod Menus & Injectors** | Executor detection, blacklisted menu signatures, resource injection |
| 💣 **Server Abuse** | Explosion spam, entity/vehicle/ped spam, weapon & object spawning |
| 💰 **Economy Exploits** | Money/item duplication, trigger abuse, event spoofing |
| 🧩 **Event Abuse** | Unprotected server events, payload tampering, event flooding |
| 🚫 **Ban Evasion** | Alt accounts, identifier spoofing, hardware ban bypasses |

## 🧠 My Approach

1. **Never trust the client.** Every important action is validated on the server.
2. **Protect every event.** Rate limits, argument checks and trigger tokens on sensitive events.
3. **Layered detection.** One signal is a suspicion, several signals are a ban. This keeps false positives low.
4. **Evidence first.** Logs, screenshots and timestamps back every ban so staff can verify it.
5. **Performance matters.** A protection that lags the server is not a protection.

## 🧪 Example: Server-Side Event Validation

```lua
-- Never trust the client: validate the source, the arguments and the rate.
RegisterNetEvent('shop:buyItem', function(item, amount)
    local src = source

    if type(item) ~= 'string' or type(amount) ~= 'number' then
        return flagPlayer(src, 'invalid_payload')
    end

    if amount < 1 or amount > MAX_AMOUNT or not Config.Items[item] then
        return flagPlayer(src, 'out_of_range')
    end

    if isRateLimited(src, 'shop:buyItem', 1000) then
        return flagPlayer(src, 'event_flood')
    end

    -- Price and balance are checked on the server, never sent by the client.
    processPurchase(src, item, amount)
end)
```

## 🧱 How a Detection Works

```
 Player action
      │
      ▼
 ┌─────────────┐   ┌──────────────┐   ┌─────────────┐   ┌──────────────┐
 │  Detection  │ → │ Verification │ → │  Evidence   │ → │  Punishment  │
 │   signal    │   │ (multi-check)│   │ log + proof │   │ warn/kick/ban│
 └─────────────┘   └──────────────┘   └─────────────┘   └──────────────┘
```

## 🛠️ Skills

![Lua](https://img.shields.io/badge/Lua-2C2D72?style=flat-square&logo=lua&logoColor=white)
![FiveM](https://img.shields.io/badge/FiveM-F40552?style=flat-square&logo=fivem&logoColor=white)
![ESX](https://img.shields.io/badge/ESX-2ea44f?style=flat-square)
![QBCore](https://img.shields.io/badge/QBCore-00D4FF?style=flat-square)
![Discord](https://img.shields.io/badge/Discord%20Logging-5865F2?style=flat-square&logo=discord&logoColor=white)

`Exploit analysis` · `Event security` · `Log analysis` · `Server hardening` · `Ban management` · `Cheat research` · `Incident response`

---

<div align="center">

*A fair server is a thriving server.*

</div>
