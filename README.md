# UEAbilitySurvival

Developed with Unreal Engine 5
## Features
### Generic Ability System
Modular RPG ability system and procedurally spawned enemies using Unreal Engine's Blueprints and C++. Enemies spawn in different types to enhance the utility and uniqueness of each ability, resulting in an engaging, replayable, and strategical gameplay loop.
I initially programmed a generic RPG ability infrastructure along with two abilities (Flamethrower and Fire Ball), along with a HUD that can be interacted with both mouse and keyboard, while the buttons also change their style depending on if there's an active ability or not. Then I added an Ability Rotation system that puts used abilities on a queue and progressively gives them back to the player as long as there is open space in the Hotbar. I used a couple of icon assets from a YouTube tutorial and some sounds from ZapSplat.

I programmed a generic class called GameplayAbility that is then used as a base for the rest of the abilities and it contains two main functions. Activate and Deactivate, which can be used to create abilities that can be channeled.
For the Flamethrower (channeling ability) the character stops and has reduced rotation speed in order to give a feeling of weight to the ability and then plays a Niagara system effect that sends fire particles that are intended to later deal damage and potentially be used to interact with flammable parts in the environment Then, the ability Fireball spawns a cylinder with a fire Niagara System that is similar other one in the flamethrower. Both abilities play a fitting sound when triggered.

## Design Goals

I intend to create a gameplay-focused game that takes advantage of MMO elements like a big variety of abilities but in a more simplified form. These will have different strengths and weaknesses. For instance, AoE/Single Target, Instant Heal/HoT, Common but Weak / Rare but Powerful, and more constraints that force the player to strategize and adapt to increasingly difficult waves of enemies.
I intend to make it a Survival game with a style similar to an arcade game, for which the player's goal will be to survive the most amount of waves. These would be composed by enemies with different sizes, and health, and they would appear at different rates and in different formations.
Ideally, I would like to add levels with interactable environments with a beginning and a goal point if possible but considering that would take a lot of time, I may not be able to do it for now. Additionally, there are a lot of possible QoL details like a HUD indicator for the next ability in rotation but for now, I'd like to prioritize making a playable prototype with enemies and a basic system of waves and win/loss states.
