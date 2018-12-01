---
permalink: /modules
title: Module Directory
classes: page--modules

categories:
- header: Skill Predictors
  description: "Simulates skills client-side so you can evade taxes of the ping variety."
  modules:
  - repo: tera-mods/skill-prediction
    desc: The big one. Supports most skills.
- header: Notable Modules
  description: "The big guns. These modules are more than simple scripts."
  modules:
  - repo: caali/battle-notify
    desc: Shows text notifications on configurable in-game events.
- header: Quality of Life
  description: "These modules are relatively benign, and there's likely little risk to using these. But they *will* make your life better, probably."
  modules:
  - repo: TeraProxy/AFKer
    desc: Prevents the client from going back to character selection.
  - repo: tera-mods/auto-vanguard
    author: Pinkie Pie
    desc: Automatically turns in Vanguard quests upon completion.
  - repo: teralove/camera-distance
    desc: Removes limit on the camera's max range.
  - repo: teralove/channel-command
    desc: Switch channels via chat command.
  - repo: TeraProxy/EnrageNotifier
    desc: Shows private party notices for enrage and next enrage percentage.
  - repo: teralove/exit-command
    desc: Exit the game via chat command.
  - repo: teralove/exit-instantly
    desc: Exit the game without having to wait 10 seconds. (Basically clicking the X button.)
  - repo: teralove/lobby-command
    desc: Return to lobby (character select) via chat command.
  - repo: Mister-Kay/no-more-crazy-capes
    desc: Removes exploding physics glitch from some back items.
  - repo: teralove/parcel-helper
    desc: Instantly accept all parcels and delete all read messages.
  - repo: teralove/party-death-markers
    desc: Shows rare item beacon on party member corpses.
  - repo: Snugglez/relog
    desc: Switch character via chat command.
  - repo: caali-hackerman/skill-resets
    desc: Pops up a message whenever a skill resets.
  - repo: tera-mods/no-cutscenes
    author: Pinkie Pie
    desc: No more mashing Esc after killing a boss. Pretend cutscenes don't even exist.
  - repo: Saegusae/looks
    desc: Copies the character's appearance of yourself or other nearby players.
- header: The Questionable Ones
  description: "Where the line starts getting blurred. If you use these and it gets noticed... Well, no promises."
  modules:
  - repo: tera-mods/auto-negotiate
    author: Pinkie Pie
    desc: Automatically accepts or declines broker negotiations. Configurable.
  - repo: TeraProxy/Essentials
    desc: Automatically uses Nostrum/Battle Solution" and Complete Crystalbind items whenever needed.
  - repo: TeraProxy/Cosplayer
    desc: Allows wearing anything client-sided through UI selection.
  - repo: tera-mods/fly-forever
    author: Pinkie Pie
    desc: Ignores flying mount stamina for infinite flying.
  - repo: Risenio/fps-utils
    desc: A compilation of utilities to improve fps, includes disabling fireworks effects.
  - repo: Risenio/let-me-pot
    desc: Automatically uses HP or MP potions at certain % you choose & has slay support.
  - repo: Risenio/let-me-drink
    desc: Automatically uses "Lein's Dark Root Beer" at certain usage of skills.
  - repo: Risenio/let-me-lock
    desc: Automatically locks on players for healing/cleansing | npcs for debuff/dps purposes.
  - repo: teralove/auto-heal
    desc: Automatically skips lockons and instantly heals and cleanses party members.
  - repo: TeraProxy/Teabagger
    desc: Allows you teabag people. but rly tho?
  - repo: Saegusae/loot
    desc: Automatically loots items in a radius upon pressing F on an item.
---

Here is a directory with links to a number of GitHub projects and developers who work with tera-proxy or other TERA modding programs. That means **all projects directly linked here are free and open source**.

If you want to be added to this list, or you think a module has been miscategorized, [submit a PR](https://github.com/meishuu/tera-proxy/edit/gh-pages/_pages/modules.md).

{% for category in page.categories %}
{% assign names = "" | split: "" | where_exp: "item", "false" %}
{% for module in category.modules %}
{% assign repo = module.repo | split: "/" | last | downcase %}
{% assign names = names | push: repo %}
{% endfor %}
{% assign names = names | uniq | sort %}

## {{ category.header }}

{{ category.description }}

| Module | Description |
| --- | --- |{% for name in names %}{% for module in category.modules %}{% assign repo = module.repo | split: "/" %}{% assign test = repo | last | downcase %}{% if test != name %}{% continue %}{% endif %}{% assign user = module.author %}{% unless user %}{% assign user = repo[0] %}{% endunless %}
| [{% avatar user=user %}][@{{ user }}] [{{ repo[1] }}](https://github.com/{{ module.repo }}) | {{ module.desc }} |{% endfor %}{% endfor %}

{% endfor %}

## Module Developers

For any other kind of module, you may want to take a look at public repositories or websites. Below is a list of module developers on GitHub, along with links to other sources where you may find more information or modules not publicly posted.

* [{% avatar pinkipi %} pinkipi][@PinkiePie] &ndash; [Discord](https://discord.gg/RR9zf85)
* [{% avatar caali-hackerman %} caali-hackerman][@caali] &ndash; [Discord](https://discord.gg/dUNDDtw)
* [{% avatar Saegusae %} Saegusae][@Saegusae]
* [{% avatar teralove %} teralove][@teralove]
* [{% avatar TeraProxy %} TeraProxy][@TeraProxy]

## Related Projects

tera-proxy is just one of many projects aimed at modding and extending TERA functionality. These related projects are not modules; they are standalone programs that do their own thing with or without tera-proxy.

* [ShinraMeter](https://github.com/neowutran/ShinraMeter) ([@neowutran], [@Gl0]): A TERA DPS meter. &ndash; [Discord](https://discord.gg/anUXQTp)
* [Tera Custom Cooldowns](https://github.com/Foglio1024/Tera-custom-cooldowns) ([@Foglio1024]): Replaces some TERA UI elements with sleek and responsive designs. &ndash; [Discord](https://discord.gg/anUXQTp)



[//]: # (GitHub @mention link references go below.)

[@Foglio1024]: <https://github.com/Foglio1024> "Foglio"
[@Gl0]: <https://github.com/Gl0> "Gl0"
[@Mister-Kay]: <https://github.com/mister-kay>
[@neowutran]: <https://github.com/neowutran> "Yukikoo"
[@PinkiePie]: <https://github.com/tera-mods> "Pinkie Pie"
[@Saegusae]: <http://github.com/saegusae> "Seagoose"
[@teralove]: <https://github.com/teralove>
[@TeraProxy]: <https://github.com/TeraProxy>
[@caali]: <https://github.com/caali-hackerman>