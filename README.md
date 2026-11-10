# XLondon

XLondon is a solo tactical squad game played across the real streets of London. Choose three or four operatives from a persistent roster, scout the area in WorldLens on Quest 2, and use a companion dashboard to generate encounters and run the rules.

This is a design brief. The core rules are provisional, and the setting is open.

## Playing in WorldLens

WorldLens supplies the terrain. Missions take place outdoors and can spill across several connected streets. You can fly around to inspect an approach without moving an operative or spending an action. Judge where the squad can move, what it can see, and what offers cover from the relevant direction.

Use landmarks as natural position labels, such as “museum entrance, Great Russell Street” or “the corner on Montagu Place.” These are reminders, not fixed movement zones. A fictional encounter near the British Museum might start on Great Russell Street, shift into Montagu Place, and end near Russell Square.

Naming roads, junctions and points of interest as you play provides incidental Knowledge of London practice. It carries no score, bonus or penalty.

## Google Earth Web character cards

To use a placemark as a miniature on the 3D map, open a Google Earth Web project on your laptop, add a placemark, and open the HTML editor for its description. Paste the complete snippet for your display mode, then save the placemark. Edit the name, role, stats and weapon in the snippet for each miniature. The Soldier values below are examples for testing the card layout.

### Light mode

```html
<div style="max-width:270px; background:#f1f3e9; border:1px solid #495447; border-radius:8px; overflow:hidden; font-family:Arial,sans-serif;">
  <div style="background:#344432; padding:12px 14px;">
    <div style="font-size:10px; letter-spacing:2px; color:#d6e5cd;">
      XLONDON / SQUAD 01
    </div>
    <div style="font-size:22px; font-weight:bold; color:#ffffff; margin-top:3px;">
      Soldier
    </div>
    <div style="font-size:12px; color:#e0ebd9;">
      Rifleman · S-01
    </div>
  </div>

  <div style="padding:12px 14px;">
    <table style="width:100%; border-collapse:collapse; text-align:center;">
      <tr style="font-size:10px; letter-spacing:1px;">
        <th style="color:#40513b;" scope="col">HP</th>
        <th style="color:#40513b;" scope="col">MOVE</th>
        <th style="color:#40513b;" scope="col">ACTION</th>
        <th style="color:#40513b;" scope="col">AIM</th>
      </tr>
      <tr style="font-size:20px; font-weight:bold;">
        <td style="color:#172017;">4</td>
        <td style="color:#172017;">2</td>
        <td style="color:#172017;">2</td>
        <td style="color:#172017;">+1</td>
      </tr>
    </table>

    <div style="border-top:1px solid #b8c1ad; margin-top:10px; padding-top:9px; font-size:12px;">
      <strong style="color:#172017;">Assault rifle</strong><br>
      <span style="color:#40513b;">Medium range · 1 damage</span>
    </div>
  </div>
</div>
```

### Dark mode

The dark wrapper fills the white description area around the card. The `356px` width and `-16px` margin matched the tested Google Earth Web popup on the laptop. If the popup is a different width, adjust the wrapper width to match. The stat panel stays light for readability.

```html
<div style="background:#191b19; margin:-16px; padding:16px; width:356px; box-sizing:border-box;">
  <div style="max-width:270px; background:#f1f3e9; border:1px solid #495447; border-radius:8px; overflow:hidden; font-family:Arial,sans-serif;">
    <div style="background:#344432; padding:12px 14px;">
      <div style="font-size:10px; letter-spacing:2px; color:#d6e5cd;">
        XLONDON / SQUAD 01
      </div>
      <div style="font-size:22px; font-weight:bold; color:#ffffff; margin-top:3px;">
        Soldier
      </div>
      <div style="font-size:12px; color:#e0ebd9;">
        Rifleman · S-01
      </div>
    </div>

    <div style="padding:12px 14px;">
      <table style="width:100%; border-collapse:collapse; text-align:center;">
        <tr style="font-size:10px; letter-spacing:1px;">
          <th style="color:#40513b;" scope="col">HP</th>
          <th style="color:#40513b;" scope="col">MOVE</th>
          <th style="color:#40513b;" scope="col">ACTION</th>
          <th style="color:#40513b;" scope="col">AIM</th>
        </tr>
        <tr style="font-size:20px; font-weight:bold;">
          <td style="color:#172017;">4</td>
          <td style="color:#172017;">2</td>
          <td style="color:#172017;">2</td>
          <td style="color:#172017;">+1</td>
        </tr>
      </table>

      <div style="border-top:1px solid #b8c1ad; margin-top:10px; padding-top:9px; font-size:12px;">
        <strong style="color:#172017;">Assault rifle</strong><br>
        <span style="color:#40513b;">Medium range · 1 damage</span>
      </div>
    </div>
  </div>
</div>
```

## Core rules

| Rule | Working version |
| --- | --- |
| Squad | Deploy **3–4 operatives** from a persistent roster. Six starting operatives is a proposed test roster. |
| Operative | Name, **3 Health**, one weapon, one speciality and one limited-use ability. |
| Round | The squad acts first, then the enemies. Each operative gets **two actions**. |
| Actions | **Move**, **Shoot**, **Overwatch** or **Interact**. Interact covers objectives and helping casualties. |
| Distance | **Near**, **Medium** or **Far**, judged visually from the acting character. Different squad members can be at different ranges from the same target. |
| Movement | One Move repositions locally or closes one range band when the route allows it. Follow plausible street routes around obstacles. |
| Line of sight | Solid buildings and walls block sight. Check cover from the attacker’s direction. |
| Shooting | Roll **1d6**. A **4+** hits an exposed target and a **5+** hits one in cover. A standard hit deals **1 damage**. |
| Weapon ranges | Proposed starting profile. Shotgun **Near**, rifle **Near or Medium**, sniper rifle **Medium or Far**. |
| Overwatch | End the operative’s turn ready to shoot the first enemy that moves into sight and effective range before the next squad turn. |
| Casualties | At **0 Health**, an operative is down and cannot act. A nearby teammate can spend an Interact action to carry them, moving more slowly. An operative left behind is lost under the initial rules. |

Start with one use of each speciality per mission. Example abilities include a Medic restoring 1 Health, a Scout taking a free Move, and a Heavy dealing 1 damage to enemies in a small area with a grenade. A Technician could help with objectives. The first test can use fixed damage and omit ammunition and reload tracking.

## Encounters and the dashboard

The dashboard generates an incident and enemy cards. The player places the generated elements in the WorldLens scene where they make sense.

| Generated detail | Examples |
| --- | --- |
| Opposition | Usually **1–3 enemies** for an initial encounter. Scale later encounters to the deployed squad and mission. |
| Starting range | Near, Medium or Far from the squad’s entry point. |
| Position aspect | Exposed, in cover, elevated or concealed. This describes the starting position and can change in play. |
| Weapon and trait | Close-range weapon, rifle or sniper rifle. Occasional traits include armoured, fast, accurate, medic or leader. |
| Behaviour | Hold and shoot, advance, guard, flank, retreat or pursue an objective. |

Most enemies should be ordinary. A proposed difficulty budget would let extra enemies and special abilities draw on the same allowance. Generate combinations that make sense, such as a shotgun enemy who can close the distance. If an aspect does not fit the visible terrain, reroll it. Unidentified contacts can stay hidden until an operative gets a usable view.

For the first test, an ordinary enemy has **1 Health and one action**. Its default behaviour is to shoot the nearest visible target it can hit, or move towards its objective if it has no shot. Break ties randomly. Specialists can have their own simple priority.

The dashboard tracks health, actions, equipment, ability uses, overwatch, enemies, rounds and objective progress. For a shot, select the attacker and target, confirm range and cover, then roll and apply damage. Check relative range when it matters instead of maintaining a distance table for every pair. Movement spends an action and can optionally update a short location label. An **Enemy Turn** control presents enemy intentions, asks for any spatial judgments it needs and resolves attacks. A short event log, undo and autosave would support play.

## Missions and campaign

A generated mission needs a **location, incident, objective and escalation**. Objectives include recovering evidence or equipment, escorting a contact, pursuing a courier, protecting civilians, disrupting a device or extracting a casualty. A changing rendezvous, moving target or unsafe extraction point can carry play into another street. Use turn limits or reinforcements for urgency.

The campaign loop is **briefing → select squad and equipment → deploy → resolve the objective and extract → debrief**. Survivors develop, injured operatives may miss missions, and replacements start inexperienced. Equipment can belong to the organisation and be assigned at deployment.

Jobs can stand alone or lead to others. Some incidents only reveal their connection later, when the same contact, equipment or organisation turns up again. Recovering evidence can unlock follow-up missions, an enemy weakness or a piece of equipment. A simple research option is three recovered clues for a discovery.

## Setting candidates

| Setting | What generates missions | Campaign direction |
| --- | --- | --- |
| **Alien invasion** | Sightings, abductions, crash-site recoveries and civilian emergencies. | Investigate the threat, learn its capabilities and turn discoveries into a counterattack. |
| **Occupied London** | An alternate history in which Nazi forces occupy London. A resistance cell responds to prisoner transfers, patrols and compromised contacts. | Build local support, endure reprisals and potentially work towards liberation. |
| **Counterterrorism thriller** | Threat reports, suspect sightings, witness protection, rescue and urgent extractions. | Uncover a fictional network. Identification, restraint and civilian safety shape outcomes. |
| **Alternate Prohibition London** | Collections, deliveries, disputed businesses and rival activity. | Build income and influence while managing loyalties, police attention and the fallout of violence. |
| **Near-future hacker cell** | A *Watch Dogs*-style field team takes contracts, helps whistleblowers and disrupts corporate surveillance. | An open-ended job board with recurring clients and rivals. Abstract hacking can reveal contacts, distract opposition or open routes. A shared Trace track is optional. |

Freelance contracting is a campaign structure that could sit within the hacker setting or stand on its own. A short job board gives the player a choice of objectives, risks and rewards.

## Ideas to test after the core encounter

- **XCOM (1994).** Start with incidents and an unfamiliar enemy. Recovery and research reveal what is happening and how to respond. Treat the deployed squad as one field team supported by a larger organisation.
- **XCOM (2012).** Let discoveries unlock specific operations. Use a small support cast to give briefings and conflicting priorities. An operative from the roster can become important through play.
- **Star Wars Zero Company.** Resolve routine assignments quickly and play consequential missions in detail. Bonds can affect how operatives work together.
- **Commandos.** Give guards short, readable patrol routes between landmarks. Test distractions, complementary specialists and a shared **Unaware → Suspicious → Alarm** track. Let squad members spend their actions in any order so one can create an opening for another.
- **Rainbow Six.** Scout the area before deployment and choose an approach and extraction point using incomplete intelligence. Test one **Go Code** that lets two operatives execute preassigned orders on a shared trigger, spending their remaining actions.
- **SWAT 2 and Rainbow Six.** Let separate call-outs acquire a second meaning when evidence links some of them to the same organisation. For police scenarios, surrender, rescue and a clean extraction can matter more than defeating the opposition.
- **Nemesis-style continuity.** Let recurring rivals remember what happened and change position between encounters. A defeated rival might flee, lose standing or return with an ally.

## Tabletop comparisons

- **Battlespace** is the closest modern military comparison for short solo missions and automated opposition. Its standard fireteam has four soldiers.
- **Five Parsecs from Home** is a reference for a persistent roster and generated campaigns. **Bug Hunt** follows a small core cast but can add supporting troops in play.
- **Five Men in Normandy** is a WWII reference for recurring soldiers and small-unit campaign play.
- **Sellswords & Spellslingers** is a fantasy solo skirmish game that supports a three-character party. **Rangers of Shadow Deep** and **Space Station Zero** are references for linked scenarios, with more figures on the table.

## First playtest

Use **three operatives, three basic enemies, one objective and one extraction point** in a small outdoor area. Recover an item and extract before the end of round six. Place everyone using visible landmarks and judge range only when it matters. Use the results to see whether WorldLens makes movement and cover interesting and whether the dashboard keeps turns moving.
