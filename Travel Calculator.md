---
tags: []
MilesPerHour: 3
SpeedMultiplier: 1
TemperatureMaxTravelHours: 4
HoursPerDay: 5
TravelDistance: 4000
MinutesInDay: "1440"
---


# Travel Speed
| PF2e Travel Calculator                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Party Speed (slowest):** `INPUT[inlineSelect(option(1, 10 Feet), option(1.5, 15 Feet), option(2, 20 Feet), option(2.5, 25 Feet),  option(3, 30 Feet),  option(3.5, 35 Feet),  option(4, 40 Feet),  option(5, 50 Feet),  option(6, 60 Feet),  option(50, 500 Feet)):MilesPerHour]`                                                                                                                                                                                                                                            |
| **Terrain Type:** `INPUT[inlineSelect(option(1, Normal Terrain), option(0.5, Difficult Terrain), option(0.333333, Greater Difficult Terrain)):SpeedMultiplier]`                                                                                                                                                                                                                                                                                                                                         |
| **Temperature:** `INPUT[inlineSelect(option(2, Incredible Cold - Moderate dmg every minute), option(4, Extreme Cold - Minor cold dmg every 10 minutes), option(4, Severe Cold - Minor cold dmg every hour), option(4, Mild Cold - None), option(8, Normal - None), option(4, Mild Heat - None), option(4, Severe Heat - Minor fire dmg every hour), option(4, Extreme Heat - Minor fire dmg every 10 minutes), option(2, Incredible Heat - Moderate fire dmg every minute)):TemperatureMaxTravelHours]` |
| **Max Travel Hours Per Day:** `VIEW[round({TemperatureMaxTravelHours},1)]`                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Travel Hours Per Day:** `INPUT[number:HoursPerDay]` `VIEW[{HoursPerDay}>{TemperatureMaxTravelHours} ? "Suffer Fatigue" : "No Fatigue"]`                                                                                                                                                                                                                                                                                                                                                               |
| **Miles To Travel:**  `INPUT[number:TravelDistance]`                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Distance Travelled Per Day:** `VIEW[round({MilesPerHour}*{HoursPerDay},1)]`  miles                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Days Travel 🕓:** `VIEW[round({TravelDistance} / (({MilesPerHour}*{HoursPerDay})*{SpeedMultiplier}),1)]`                                                                                                                                                                                                                                                                                                                                                                                              |
| **Minutes Travel 🕓:** `VIEW[round({TravelDistance} / ({MilesPerHour} * {SpeedMultiplier}) * 60, 1)]`                                                                                                                                                                                                                                                                                                                                                                                                   |

## Speed Examples 

| Mount | Speed |
| ---- | ---- |
| Riding Pony | 35 Feet |
| War Pony | 35 Feet |
| Riding Horse | 40 Feet |
| War Horse | 40 Feet |

| Vehicle | Speed |
| ---- | ---- |
| Sand Skiff | 500 Feet (4 hours on/2 hours off) |
| TBD | 0 Feet |
| TBD | 0 Feet |
| TBD | 0 Feet |

## Environmental Damage

| **Category** | **Damage** |
| ------------ | ---------- |
| Minor        | 1d6-2d6    |
| Moderate     | 4d6-6d6    |
| Major        | 8d6-12d6   |
| Massive      | 16d6-24d6  |

## Exploration Mode
While encounters use rounds for combat, exploration is more free form. The GM determines the flow of time, as you could be traveling by horseback across craggy highlands, negotiating with merchants, or delving in a dungeon in search of danger and treasure. Exploration lacks the immediate danger of encounter mode, but it offers its own challenges.

Much of exploration mode involves movement and roleplaying. You might be traveling from one town to another, chatting with a couple of merchants an outpost along the way, or maybe having a terse conversation with the watchful city guards at your destination. Instead of measuring your rate of movement in 5-foot squares every round, you measure it in feet or miles per minute, hour, or day, using your travel speed. Rather than deciding on each action every turn, you’ll engage in an exploration activity, and you’ll typically spend some time every day resting and making your daily preparations.

### Exploration Activities
While you're traveling and exploring, tell the GM what you'd generally like to do along the way. If you do nothing more than make steady progress toward your goal, you move at the full travel speeds given in Table 9–2.

When you want to do something other than simply travel, you describe what you are attempting to do. It isn't necessary to go into extreme detail, such as “Using my dagger, I nudge the door so I can check for devious traps.” Instead, “I'm searching the area for hazards” is sufficient. The GM finds the best exploration activity to match your description and describes the effects of that activity. Some exploration activities limit how fast you can travel and be effective.

#### Affix a Talisman
**Requirements** You must use a repair kit.

You spend 10 minutes affixing a talisman to an item, placing the item on a stable surface and using the repair kit with both hands. You can also use this activity to remove a talisman. Attaching more than one talisman to an item deactivates all the talismans. They must be removed and re-affixed before they can be used again.

#### Avoid Notice
You attempt a Stealth check to avoid notice while traveling at half speed. If you have the Swift Sneak feat, you can move at full Speed rather than half, but you still can’t use another exploration activity while you do so. If you have the Legendary Sneak feat, you can move at full Speed and use a second exploration activity. If you’re Avoiding Notice at the start of an encounter, you usually roll a Stealth check instead of a Perception check both to determine your initiative and to see if the enemies notice you (based on their Perception DCs, as normal for Sneak, regardless of their initiative check results).

#### Borrow an Arcane Spell
If you’re an arcane spellcaster who prepares from a spellbook, you can attempt to prepare a spell from someone else’s spellbook. The GM sets the DC for the check based on the spell’s level and rarity; it’s typically a bit easier than Learning the Spell.

**Success** You prepare the borrowed spell as part of your normal spell preparation.\
**Failure** You fail to prepare the spell, but the spell slot remains available for you to prepare a different spell. You can’t try to prepare this spell until the next time you prepare spells.

#### Call Companion
You spend 1 minute calling for a different animal companion, switching your active companion for another of your animal companions.

#### Cleanse Soul Path
You meditate, pray, or otherwise try to reinforce your soul's connection to your soulforged armament. This takes 10 minutes. Attempt a counteract check against your *soulforged corruption*. The counteract level is half your level rounded up, and the counteract check modifier is your religions modifier. If successful, reduce the stage of your *soulforged corruption* by 1 (to a minimum of Stage 1).

#### Coerce
With threats either veiled or overt, you attempt to bully a creature into doing what you want. You must spend at least 1 minute of conversation with a creature you can see and that can either see or sense you. At the end of the conversation, attempt an Intimidation check against the target's Will DC, modified by any circumstances the GM determines. The attitudes referenced in the effects below are summarized in the Changing Attitudes sidebar and described in full in the Conditions page.

**Critical Success** The target gives you the information you seek or agrees to follow your directives so long as they aren't likely to harm the target in any way. The target continues to comply for an amount of time determined by the GM but not exceeding 1 day, at which point the target becomes unfriendly (if they weren't already unfriendly or hostile). However, the target is too scared of you to retaliate—at least in the short term.\
**Success** As critical success, but once the target becomes unfriendly, they might decide to act against you—for example, by reporting you to the authorities or assisting your enemies.\
**Failure** The target doesn’t do what you say, and if they were not already unfriendly or hostile, they become unfriendly.\
**Critical Failure** The target refuses to comply, becomes hostile if they weren’t already, and can’t be Coerced by you for at least 1 week.

#### Compose Missive
You spend 10 minutes drawing, writing, or inscribing, covering the missive's surface with text, images, or embossing.

#### Cover Tracks
You cover your tracks, moving up to half your travel speed. You don’t need to attempt a Survival check to cover your tracks, but anyone tracking you must succeed at a Survival check against your Survival DC if it is higher than the normal DC to Track.

In some cases, you might Cover Tracks in an encounter. In this case, Cover Tracks is a single action and doesn’t have the exploration trait.

#### Decipher Writing
You attempt to decipher complicated writing or literature on an obscure topic. This usually takes 1 minute per page of text, but might take longer (typically an hour per page for decrypting ciphers or the like). The text must be in a language you can read, though the GM might allow you to attempt to decipher text written in an unfamiliar language using Society instead.

The DC is determined by the GM based on the state or complexity of the document. The GM might have you roll one check for a short text or a check for each section of a larger text.

**Critical Success** You understand the true meaning of the text.\
**Success** You understand the true meaning of the text. If it was a coded document, you know the general meaning but might not have a word-for-word translation.\
**Failure** You can’t understand the text and take a –2 circumstance penalty to further checks to decipher it.\
**Critical Failure** You believe you understand the text on that page, but you have in fact misconstrued its message.

##### Sample Decipher Writing Tasks

**Trained** entry-level philosophy treatise\
**Expert** complex code, such as a cipher\
**Master** spymaster’s code or advanced research notes\
**Legendary** esoteric planar text written in metaphor by an ancient celestial

#### Defend
You move at half your travel speed with your shield raised. If combat breaks out, you gain the benefits of Raising a Shield before your first turn begins.

##### Raise a Shield\[one-action]
**Requirements** You are wielding a shield.

You position your shield to protect yourself. When you have Raised a Shield, you gain its listed circumstance bonus to AC. Your shield remains raised until the start of your next turn.

#### Detect Magic
You cast *detect magic* at regular intervals. You move at half your travel speed or slower. You have no chance of accidentally overlooking a magic aura at a travel speed up to 300 feet per minute, but must be traveling no more than 150 feet per minute to detect magic auras before the party moves into them.

#### Enter the Harrow Court
You concentrate on a card from the *Deck of Destiny* that you have invested, focusing on it as if you were looking through a window rather than at a piece of artwork. After 1 minute, a stationary portal appears in the air in front of you, its edges resembling the quick riffling of a thick deck of cards. You and any other creatures you designate can pass through this portal to enter the Harrow Court, arriving in a fortress at the center of the demiplane known as the Harrowheart. (As you continue to epitomize more cards within the Harrow Court, you unlock new areas into which you can potentially arrive as well—but in this adventure, that ability won't yet be granted.) Once created, the portal persists for up to 1 minute or until you take an action with the envision trait to close the portal.

A character in the Harrow Court can use this activity to open a portal out of the demiplane, but this portal always leads to the same point in the multiverse they were at when they previously entered the Harrow Court (unless certain cards have been epitomized to allow more options).

#### Follow the Expert
Choose an ally attempting a recurring skill check while exploring, such as climbing, or performing a different exploration tactic that requires a skill check (like Avoiding Notice). The ally must be at least an expert in that skill and must be willing to provide assistance. While Following the Expert, you match their tactic or attempt similar skill checks. Thanks to your ally’s assistance, you can add your level as a proficiency bonus to the associated skill check, even if you’re untrained. Additionally, you gain a circumstance bonus to your skill check based on your ally’s proficiency (+2 for expert, +3 for master, and +4 for legendary).

#### Gather Information
You canvass local markets, taverns, and gathering places in an attempt to learn about a specific individual or topic. The GM determines the DC of the check and the amount of time it takes (typically 2 hours, but sometimes more), along with any benefit you might be able to gain by spending coin on bribes, drinks, or gifts.

**Success** You collect information about the individual or topic. The GM determines the specifics.\
**Critical Failure** You collect incorrect information about the individual or topic.

##### Sample Gather Information Tasks

**Untrained** talk of the town\
**Trained** common rumor\
**Expert** obscure rumor, poorly guarded secret\
**Master** well-guarded or esoteric information\
**Legendary** information known only to an incredibly select few, or only to extraordinary beings

#### Hustle
You strain yourself to move at double your travel speed. You can Hustle only for a number of minutes equal to your Constitution modifier × 10 (minimum 10 minutes). If you are in a group that is Hustling, use the lowest Constitution modifier among everyone to determine how fast the group can Hustle together.

#### Identify Alchemy
**Requirements** You have alchemist’s tools.

You can identify the nature of an alchemical item with 10 minutes of testing using alchemist’s tools. If your attempt is interrupted in any way, you must start over.

**Success** You identify the item and the means of activating it.\
**Failure** You fail to identify the item but can try again.\
**Critical Failure** You misidentify the item as another item of the GM’s choice.

#### Identify Magic
Once you discover that an item, location, or ongoing effect is magical, you can spend 10 minutes to try to identify the particulars of its magic. If your attempt is interrupted, you must start over. The GM sets the DC for your check. Cursed or esoteric subjects usually have higher DCs or might even be impossible to identify using this activity alone. Heightening a spell doesn’t increase the DC to identify it.

**Critical Success** You learn all the attributes of the magic, including its name (for an effect), what it does, any means of activating it (for an item or location), and whether it is cursed.\
**Success** For an item or location, you get a sense of what it does and learn any means of activating it. For an ongoing effect (such as a spell with a duration), you learn the effect’s name and what it does. You can’t try again in hopes of getting a critical success.\
**Failure** You fail to identify the magic and can’t try again for 1 day.\
**Critical Failure** You misidentify the magic as something else of the GM’s choice.

##### Magical Traditions and Skills
Each magical tradition has a corresponding skill, as shown on the table below. You must have the trained proficiency rank in a skill to use it to Identify Magic or Learn a Spell. Something without a specific tradition, such as an item with the magical trait, can be identified using any of these skills.

| **Magical Tradition** | **Corresponding Skill** |
| --------------------- | ----------------------- |
| Arcane                | Arcana                  |
| Divine                | religions                |
| Occult                | Occultism               |
| Primal                | Nature                  |

#### Impersonate
You create a disguise to pass yourself off as someone or something you are not. Assembling a convincing disguise takes 10 minutes and requires a disguise kit, but a simpler, quicker disguise might do the job if you’re not trying to imitate a specific individual, at the GM’s discretion.

In most cases, creatures have a chance to detect your deception only if they use the Seek action to attempt Perception checks against your Deception DC. If you attempt to directly interact with someone while disguised, the GM rolls a secret Deception check for you against that creature’s Perception DC instead. If you’re disguised as a specific individual, the GM might give creatures you interact with a circumstance bonus based on how well they know the person you’re imitating, or the GM might roll a secret Deception check even if you aren’t directly interacting with others.

**Success** You trick the creature into thinking you’re the person you’re disguised as. You might have to attempt a new check if your behavior changes.\
**Failure** The creature can tell you’re not who you claim to be.\
**Critical Failure** The creature can tell you’re not who you claim to be, and it recognizes you if it would know you without a disguise.

#### Investigate
You seek out information about your surroundings while traveling at half speed. You use Recall Knowledge as a secret check to discover clues among the various things you can see and engage with as you journey along. You can use any skill that has a Recall Knowledge action while Investigating, but the GM determines whether the skill is relevant to the clues you could find.

#### Learn a Spell
**Requirements** You have a spellcasting class feature, and the spell you want to learn is on your magical tradition’s spell list.

You can gain access to a new spell of your tradition from someone who knows that spell or from magical writing like a spellbook or scroll. If you can cast spells of multiple traditions, you can Learn a Spell of any of those traditions, but you must use the corresponding skill to do so. For example, if you were a cleric with the bard multiclass archetype, you couldn't use religions to add an occult spell to your bardic spell repertoire.

To learn the spell, you must do the following:

-   Spend 1 hour per level of the spell, during which you must remain in conversation with a person who knows the spell or have the magical writing in your possession.
-   Have materials with the Price indicated in Table 4–3.
-   Attempt a skill check for the skill corresponding to your tradition (DC determined by the GM, often close to the DC on Table 4–3). Uncommon or rare spells have higher DCs.

If you have a spellbook, Learning a Spell lets you add the spell to your spellbook; if you prepare spells from a list, it's added to your list; if you have a spell repertoire, you can select it when you add or swap spells.

##### Learning a Spell

| **Spell Level** | **Price** | **Typical DC** |
| --------------- | --------- | -------------- |
| 1st or cantrip  | 2 gp      | 15             |
| 2nd             | 6 gp      | 18             |
| 3rd             | 16 gp     | 20             |
| 4th             | 36 gp     | 23             |
| 5th             | 70 gp     | 26             |
| 6th             | 140 gp    | 28             |
| 7th             | 300 gp    | 31             |
| 8th             | 650 gp    | 34             |
| 9th             | 1,500 gp  | 36             |
| 10th            | 7,000 gp  | 41             |

**Critical Success** You expend half the materials and learn the spell.\
**Success** You expend the materials and learn the spell.\
**Failure** You fail to learn the spell but can try again after you gain a level. The materials aren’t expended.\
**Critical Failure** As failure, plus you expend half the materials.

#### Make an Impression
With at least 1 minute of conversation, during which you engage in charismatic overtures, flattery, and other acts of goodwill, you seek to make a good impression on someone to make them temporarily agreeable. At the end of the conversation, attempt a Diplomacy check against the Will DC of one target, modified by any circumstances the GM sees fit. Good impressions (or bad impressions, on a critical failure) last for only the current social interaction unless the GM decides otherwise.

**Critical Success** The target’s attitude toward you improves by two steps.\
**Success** The target’s attitude toward you improves by one step.\
**Critical Failure** The target’s attitude toward you decreases by one step.

#### Pursue a Lead
**Frequency** once per 10 minutes

You spend 1 minute examining the details of one potential clue, designating the subject related to that clue as the target of your active investigation. This subject is typically a single creature, item, or small location (such as a room or corridor), but the GM might allow a different scope for your investigation. You don't need to know the identity, purpose, or nature of the subject, but you do need to be aware of its existence. For instance, finding a footprint is enough to investigate the creature that left it, and seeing a hasty sketch of an item or location can be enough to start your investigation of that subject.

Whenever you attempt a Perception or skill check to investigate a designated subject, you gain a +1 circumstance bonus to the check. The exact checks this applies to depend on the actions you use to investigate and are determined by the GM, but checks to investigate are typically Perception checks or skill checks that use Intelligence, Wisdom, or Charisma.

You can maintain two active investigations at a time. If you Pursue another Lead after that, the subject must be different from any of your current investigations (or rather, they must be different as far as you know), and you give up on a current subject of your choice. Once you've given up pursuit of a subject, you can't Pursue that Lead again until after the next time you make your daily preparations.

#### Rally
**Requirements** trained in Diplomacy, Intimidation, or Performance

You spend 1 minute encouraging your ally. Though this action typically has the auditory and linguistic traits, if you’re using the Performance skill, the GM might adjust the traits for this action to match the traits for your type of performance.

Attempt a DC 15 skill check. The GM might adjust this DC based on the circumstances, such as attempting to Rally an ally who just suffered a humiliating defeat.

**Critical Success** The ally can spend 1 Resolve Point to regain all their Stamina Points.\
**Success** You can continue encouraging your ally for a total of 10 minutes. If you do, they can spend 1 Resolve Point to regain all their Stamina Points.\
**Critical Failure** The ally takes 1d8 mental damage, but this can reduce only Stamina Points, never Hit Points.

#### Refocus
**Requirements** You have a focus pool, and you have spent at least 1 Focus Point since you last regained any Focus Points.

You spend 10 minutes performing deeds to restore your magical connection. This restores 1 Focus Point to your focus pool. The deeds you need to perform are specified in the class or ability that gives you your focus spells. These deeds can usually overlap with other tasks that relate to the source of your focus spells. For instance, a cleric with focus spells from a good deity can usually Refocus while tending the wounds of their allies, and a wizard of the illusionist school might be able to Refocus while attempting to Identify Magic of the illusion school.

#### Repair
**Requirements** You have a repair kit.

You spend 10 minutes attempting to fix a damaged item, placing the item on a stable surface and using the repair kit with both hands. The GM sets the DC, but it’s usually about the same DC to Repair a given item as it is to Craft it in the first place. You can’t Repair a destroyed item.

**Critical Success** You restore 10 Hit Points to the item, plus an additional 10 Hit Points per proficiency rank you have in Crafting (a total of 20 HP if you’re trained, 30 HP if you’re an expert, 40 HP if you’re a master, or 50 HP if you’re legendary).\
**Success** You restore 5 Hit Points to the item, plus an additional 5 per proficiency rank you have in Crafting (for a total of 10 HP if you are trained, 15 HP if you’re an expert, 20 HP if you’re a master, or 25 HP if you’re legendary).\
**Critical Failure** You deal 2d6 damage to the item. Apply the item’s Hardness to this damage.

#### Repeat a Spell
You repeatedly cast the same spell while moving at half speed. Typically, this spell is a cantrip that you want to have in effect in the event a combat breaks out, and it must be one you can cast in 2 actions or fewer. In order to prevent fatigue due to repeated casting, you’ll likely use this activity only when something out of the ordinary occurs.

You can instead use this activity to continue Sustaining a Spell or Activation with a sustained duration. Most such spells or item effects can be sustained for 10 minutes, though some specify they can be sustained for a different duration.

#### Scout
You scout ahead and behind the group to watch danger, moving at half speed. At the start of the next encounter, every creature in your party gains a +1 circumstance bonus to their initiative rolls.

#### Search
You Seek meticulously for hidden doors, concealed hazards, and so on. You can usually make an educated guess as to which locations are best to check and move at half speed, but if you want to be thorough and guarantee you checked everything, you need to travel at a Speed of no more than 300 feet per minute, or 150 feet per minute to ensure you check everything before you walk into it. You can always move more slowly while Searching to cover the area more thoroughly, and the Expeditious Search feat increases these maximum Speeds. If you come across a secret door, item, or hazard while Searching, the GM will attempt a free secret check to Seek to see if you notice the hidden object or hazard. In locations with many objects to search, you have to stop and spend significantly longer to search thoroughly.

#### Sense Direction
Using the stars, the position of the sun, traits of the geography or flora, or the behavior of fauna, you can stay oriented in the wild. Typically, you attempt a Survival check only once per day, but some environments or changes might necessitate rolling more often. The GM determines the DC and how long this activity takes (usually just a minute or so). More unusual locales or those you’re unfamiliar with might require you to have a minimum proficiency rank to Sense Direction. Without a compass, you take a –2 item penalty to checks to Sense Direction.

**Critical Success** You get an excellent sense of where you are. If you are in an environment with cardinal directions, you know them exactly.\
**Success** You gain enough orientation to avoid becoming hopelessly lost. If you are in an environment with cardinal directions, you have a sense of those directions.

##### Sample Sense Direction Tasks

**Untrained** determine a cardinal direction using the sun\
**Trained** find an overgrown path in a forest\
**Expert** navigate a hedge maze\
**Master** navigate a byzantine labyrinth or relatively featureless desert\
**Legendary** navigate an ever-changing dream realm

#### Squeeze
You contort yourself to squeeze through a space so small you can barely fit through. This action is for exceptionally small spaces; many tight spaces are difficult terrain that you can move through more quickly and without a check.

**Critical Success** You squeeze through the tight space in 1 minute per 10 feet of squeezing.\
**Success** You squeeze through in 1 minute per 5 feet.\
**Critical Failure** You become stuck in the tight space. While you’re stuck, you can spend 1 minute attempting another Acrobatics check at the same DC. Any result on that check other than a critical failure causes you to become unstuck.

##### Sample Squeeze Tasks

**Trained** space barely fitting your shoulders\
**Master** space barely fitting your head

#### Take a Breather
**Cost** 1 Resolve Point

You rest for 10 minutes and recover your stamina. After you complete this activity, you regain all your Stamina Points.

#### Track
You follow tracks, moving at up to half your travel speed. After a successful check to Track, you can continue following the tracks at half your Speed without attempting additional checks for up to 1 hour. In some cases, you might Track in an encounter. In this case, Track is a single action and doesn’t have the exploration trait, but you might need to roll more often because you’re in a tense situation. The GM determines how often you must attempt this check.

You attempt your Survival check when you start Tracking, once every hour you continue tracking, and any time something significant changes in the trail. The GM determines the DCs for such checks, depending on the freshness of the trail, the weather, and the type of ground.

**Success** You find the trail or continue to follow the one you’re already following.\
**Failure** You lose the trail but can try again after a 1-hour delay.\
**Critical Failure** You lose the trail and can’t try again for 24 hours.

##### Sample Track Tasks

**Untrained** the path of a large army following a road\
**Trained** relatively fresh tracks of a rampaging bear through the plains\
**Expert** a nimble panther's tracks through a jungle, tracks obscured by rainfall\
**Master** tracks obscured by winter snow, tracks of a mouse or smaller creature, tracks left on surfaces that can't hold prints like bare rock\
**Legendary** old tracks through a windy desert’s sands, tracks after a major blizzard or hurricane

#### Treat Wounds
**Requirements** You are holding healer's tools, or you are wearing them and have a hand free

You spend 10 minutes treating one injured living creature (targeting yourself, if you so choose). The target is then temporarily immune to Treat Wounds actions for 1 hour, but this interval overlaps with the time you spent treating (so a patient can be treated once per hour, not once per 70 minutes).

The Medicine check DC is usually 15, though the GM might adjust it based on the circumstances, such as treating a patient outside in a storm, or treating magically cursed wounds. If you’re an expert in Medicine, you can instead attempt a DC 20 check to increase the Hit Points regained by 10; if you’re a master of Medicine, you can instead attempt a DC 30 check to increase the Hit Points regained by 30; and if you’re legendary, you can instead attempt a DC 40 check to increase the Hit Points regained by 50. The damage dealt on a critical failure remains the same.

If you succeed at your check, you can continue treating the target to grant additional healing. If you treat them for a total of 1 hour, double the Hit Points they regain from Treat Wounds.

The result of your Medicine check determines how many Hit Points the target regains.

##### Treat Wounds

| **Proficiency** | **DC** | **Success Healing** | **Critical Healing** |
| --------------- | ------ | ------------------- | -------------------- |
| Trained         | 15     | 2d8                 | 4d8                  |
| Expert*         | 20     | 2d8+10              | 4d8+10               |
| Master*         | 30     | 2d8+30              | 4d8+30               |
| Legendary*      | 40     | 2d8+50              | 4d8+50               |

\* Rolling against a higher DC is optional.

**Critical Success** The target regains 4d8 Hit Points, and its wounded condition is removed.\
**Success** The target regains 2d8 Hit Points, and its wounded condition is removed.\
**Critical Failure** The target takes 1d8 damage.
