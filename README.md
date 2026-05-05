# CMU-CPCS-1stED---Cosmic-Critter
Cosmic Critter Arena is a deep-space turn-based battler where players pick, battle, heal, flee, and manage critters using a live dictionary with stats, colors, search, edits, sprites, stars, effects.

Project Description:
    COSMIC CRITTER ARENA is a turn-based monster battler set
    against a deep space backdrop where bioluminescent critters
    duel one-on-one. The game runs through four screens driven
    by a state machine: a main menu, a fighter picker, the
    battle arena, and a roster manager. The player picks a
    critter, the game randomly selects a wild opponent, and the
    two trade turns until one is knocked out. ATTACK deals
    damage based on ATK minus half DEF with a minimum of 1.
    HEAL restores 25 HP and is limited to 2 uses per battle to
    force strategic timing. FLEE escapes immediately. HP bars
    scale with current health and shift green to gold to red
    as damage stacks. Each hit triggers a half-second shake and
    a 10-particle burst with gravity, and a 3-line battle log
    keeps a rolling history at the bottom of the screen.
    
    The game is built around a CRITTER CATALOG dictionary that
    stores critter names as keys and a nested dict of type, HP,
    ATK, DEF, and color as values. The dictionary drives the
    whole game: it is read every time a critter is drawn, its
    values determine damage in battle, and it can be searched,
    modified, expanded, and trimmed by the player at runtime
    through ADD, MODIFY, DELETE, and SEARCH (which uses .get()
    for safe lookup so a typo never crashes the game). Other
    features include custom-drawn sprites with type-themed glow
    rings, animated eyes that pivot to face the opponent, and
    35 twinkling background stars that pulse on independent
    phases.
                                                        
Instructions:
    To play, click one of the four buttons on the main menu.
    BATTLE opens the fighter picker where you cycle through
    your roster with the < and > arrows or the left/right
    arrow keys, then click GO! to fight a randomly chosen wild
    critter. In battle, ATTACK deals damage and ends your
    turn, HEAL restores 25 HP (the button shows how many heals
    you have left), and FLEE escapes. The opponent attacks
    automatically after a short pause and the battle log
    records each blow. The battle ends in VICTORY, DEFEAT, or
    ESCAPED. Click BACK TO MENU to return.
    
    ROSTER lets you manage your catalog: cycle with < / > or
    the arrow keys, click MODIFY to change a stat (hp, atk,
    def, or color), or DELETE to remove the current critter
    (you will be asked to type YES to confirm). From the menu,
    ADD CRITTER walks you through prompts for name, type, HP,
    ATK, DEF, and color to insert a new entry. SEARCH (.get)
    looks up a critter by name and jumps to it in the roster.
    Press Escape or B at any time to return to the menu.
