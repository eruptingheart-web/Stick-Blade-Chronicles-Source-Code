Stick Blade Chronicles

A fast, gory stick-figure sword-fighting game that runs in a single HTML file. No build step, no dependencies, no assets to download. Open it in a browser and play.

Fight through five regions, collect weapons and relics, parry projectiles back at your enemies, and take on a multi-phase final boss.

Play
Download stick-blade-chronicles.html (or clone this repo).
Open it in any modern browser (Chrome, Firefox, Edge, Safari).

To host it, rename the file to index.html and serve the folder with any static host, such as GitHub Pages, Netlify or python3 -m http.server.

Controls
Action	Keyboard / mouse	Touch
Move	A / D or arrow keys	◀ ▶
Jump	W, Space or ↑	Jump
Block (hold)	S or ↓	Block
Slash combo	J or left click	Slash
Heavy kick (breaks guard)	K or right click	Heavy
Dash (brief invulnerability)	Shift	Dash
Ultimate (when the red meter is full)	E	Ult
Pause	P or Esc	
Mute	M	

Parrying: tap block just before a hit lands to parry a melee attack. Do the same against a projectile to reflect it back at the enemy.

Features
Combat: three-hit combos, heavy kicks, dashes with invulnerability frames, input buffering, parries, guard breaks, hit-stop, screen shake and slow-motion kills.
Gore: blood sprays, persistent floor stains, and dismemberment on kills.
Ultimates: a rage meter charges as you fight. Unleash the Crimson Moon cutscene attack when it is full.
11 enemy types: Ronin, Assassin, Brute, Shogun, Archer, Bomber, Fire Mage, Frost Mage, Spectre, Monk and Oni. Each has its own special ability, and all of them are telegraphed so you can react.
14 weapons: from the balanced Katana to the Odachi, Twin Daggers, Spear, Warhammer, Venom Fang, Thunder Katana, Frost Edge and Void Reaper. Weapons add effects like crits, burn, poison, slow, stun and lifesteal.
11 relics: equip up to three passives such as Phoenix Feather (revive), Thorn Mail, Spirit Bell and War Drum.
Campaign: 5 regions of 20 levels each, with multi-wave levels, a boss at the end of every region, story cutscenes and an ending.
Final boss: a two-form fight against the Demon God with meteor rains, blade storms, shockwaves and teleport strikes.
Endless arena: infinite waves with a boss every 10 waves and a saved best score.
New Game+: restart the campaign with stronger enemies while keeping your gear.
Dojo: spend soul coins on upgrades, weapons and relics. Beating bosses can drop them for free.
Procedural audio: sound effects and music are synthesized with the Web Audio API.
Touch controls: an on-screen pad appears on touch devices.
Auto-saving: progress is stored in your browser's localStorage.
Project structure

Everything lives in one file:

stick-blade-chronicles.html   # markup, styles and all game code

The script is organized roughly in this order: data tables (regions, enemies, weapons, relics), audio, fighter logic and AI, projectiles, rendering, then input and menus. Most content is data-driven, so adding an enemy, weapon or relic is mostly a matter of adding an entry to its table:

Enemies: the AR object (plus a fire() branch for a special ability).
Weapons: the WP array.
Relics: the RL array (plus a has('id') check where the effect applies).
Regions and bosses: the V, STORY and BO arrays.
Contributing

Issues and pull requests are welcome. Ideas that would be especially fun:

Elite enemy modifiers and daily challenges
A skill tree
More regions, bosses and weapons
Gamepad support
Better mobile layout and sound options

If you change gameplay numbers, please play a few levels to check the difficulty curve still feels right.

Save data

Progress is saved in localStorage under the key sbc2. Use Reset progress on the main menu to erase it.

License

Released under the MIT License.
