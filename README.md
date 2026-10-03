# Shank Access

Shank Access makes Shank, Klei Entertainment's 2010 side-scrolling brawler, playable without sight. It reads the
menus aloud, announces what happens in a fight, and adds positional sounds for ledges, jumps, pickups, enemies and
hazards. Its waypoint mode can guide you from one checkpoint to the next, one move at a time.

This is a public beta, version 0.2. Every single-player level has been played from start to finish with the mod, but
you may still run into rough spots. Reports are welcome.

Shank Access was written with Claude Code, Anthropic's AI coding tool, under the direction of a blind player who
tested every change in the game.

## What you need

- The Steam version of Shank for Windows. The mod checks the game when it starts. On any other version it says
  "Shank access is disabled" and does nothing more.
- A screen reader such as NVDA or JAWS, or the Windows SAPI voices.
- A single-player game. Co-op isn't supported, because the mod follows one Shank and the co-op levels have no map
  data for its sounds.

## Installing

1. Download shank-access-setup.exe from the [latest release](../../releases/latest) and run it. It can run from any
   folder.
2. Setup searches your Steam libraries for Shank and fills in the Shank folder field. If it finds nothing, or you want
   to use a different copy, press Browse and choose the Shank folder yourself. This is the folder that contains the
   bin and data folders. To open it from Steam, right-click Shank, choose Manage, then Browse local files.
3. Press Install. Installing takes about two minutes, and a progress bar shows how far along it
   is. Setup builds the mod's level maps and routes from your own copy of the game, because the download contains
   none of Klei's files. A message tells you when it's finished. You can cancel at any point, and setup removes
   everything it had written.
4. Start Shank. After a few seconds you'll hear "Shank access loaded", followed by the key that opens the mod menu.

Close the game before running setup. If you run setup again later, it tells you which version is installed and offers
to update, reinstall or uninstall it. When you uninstall, you choose between removing the mod only and removing the mod plus your settings. Setup
never changes the game's own files, so Steam's "Verify integrity of game files" leaves the mod alone. If the mod ever
tells you it needs setup, run setup again.

## Keys

You can change every key in the mod menu except F9 and F11, and you can give each one a controller button too.

- F7 opens the mod menu. On a controller, press Back.
- F2 marks a moment for feedback (see "Reporting a problem" below).
- F9 repeats the last thing spoken. F8 repeats the last long message, such as a tutorial or a dialog.
- H tells you your health, and the boss's health during a boss fight. G tells you how many grenades you have.
- P lists the pickups nearby. T lists the things nearby that you can climb or swing on.
- N lists the enemies nearby. L locks the enemy sound onto the nearest enemy. Press it again to move to the next
  enemy, and after the last one it turns off. K does the same for special enemies only.
- E turns safe edges on or off. With safe edges on, Shank stops at a dangerous drop until you push toward it again.
- W turns waypoint mode on or off. Q tells you the next move toward the next checkpoint.
- C switches between placing the game's sounds and the enemy sounds around Shank, and placing them by the camera the
  way the original game does.
- F11 turns Shank Access off completely, and on again.

## Sounds

Under Sounds in the mod menu, Learn sounds plays every sound the mod makes and tells you what each one means.

Ledges and walls ahead of you each have their own sound. It pans left or right to match where they are, and its
pitch rises or falls to show whether they're above or below you. Anything nearby that you could jump to makes a
plucked string, which repeats faster as you get closer. When the jump you would make right now, at your current
speed and direction, would land on it, you hear a short rising chirp instead. Pickups, enemies, enemy attacks and
hazards such as rockets, falling rocks and fire all have their own sounds. In waypoint mode, a chime marks the next
checkpoint.

## Waypoint mode

Press W to start. The chime leads you toward the next checkpoint, and only the next thing on the route makes a jump
sound. Press Q to hear the next move, for example "walk 10 tiles right, then long jump to swing point, 7 tiles
right, 3 tiles up". Shank is about two and a half tiles tall. To hear each move as soon as you finish the one before
it, turn on Speak each move in the Navigation category of the mod menu.

## The mod menu

F7 opens the menu and pauses the game. Up and Down move through the items. Enter opens a category or changes a
setting, and Left and Right adjust values. Escape or Backspace goes back a level, and Escape at the top level, or F7,
closes the menu. Each item ends with a sentence that explains what it does.

The categories are Speech, Sounds, Navigation, Enemies, Status and pickups, and General. In Speech you can send each
kind of message to your screen reader or to a SAPI voice, and set the voice's rate and volume. To change a key, move
to it, press Enter, then press the new key. Your settings are saved as soon as you change them.

### Controller support

Shank Access works with an Xbox-style controller (any controller Windows treats as an XInput controller). Out of the
box only one button is set: Back opens the mod menu. Every other key can be given a controller button in the menu.

Inside the menu, the D-pad or the left stick moves through the items like the arrow keys, A works like Enter, and B
or Back goes back a level. At the top level, either one closes the menu.

To give a key a controller button, find the key in the menu. Just below it is its controller button item. Press Enter
on that item, then press the button you want. You can also hold several buttons together and let go, and that
combination becomes the binding. Escape cancels, and Delete clears an existing binding.

Some limits apply:

- The mod only listens to the first controller connected.
- Buttons the game already uses can't be given to the mod, because pressing them would also act in the game. The
  game's own bindings are checked, including any changes you make on its Controls screen. Start always belongs to
  the game, and so do the right stick's left and right directions. With the game's default controls, the free inputs
  are the right stick's up and down and pressing either stick, plus combinations of those. Back is already the mod
  menu's button, so it can't be part of another binding.
- F9 and F11 can't be given a controller button.
- The comment window that opens after F2 needs a keyboard for typing.

## Reporting a problem

When something sounds wrong, confuses you, or leaves you stuck, press F2. The mod records where you are and what it
was doing. Then a small window opens where you can type what happened. Press Enter to save your comment, or Escape
to skip it.

If you made at least one mark during a session, the mod packs that session's logs into a single zip file when the
game closes. You'll find it in your Documents folder, under Shank Access and then logs. Its name is shank-access
followed by the date and time, for example shank-access-2026-10-03_09-20-46.zip. Sessions without a mark aren't
saved, and only the newest 30 zip files are kept.

To report the problem, [open an issue](../../issues/new/choose) and attach that session's zip file.

## Building from source

The source zip attached to each [release](../../releases) contains the full source for that version: C++ for the mod
itself, and Python tools for setup and development. You'll need Visual Studio 2022 with the x86 compiler, CMake, and
Python 3 with the packages listed in requirements.txt. CLAUDE.md and the docs folder describe the project's layout and the build commands. The source
doesn't include any files made from the game. Setup creates them from your copy of Shank, and tools/deploy.py does
the same during development.

## Licence

Shank Access is released under the MIT licence (see LICENSE). The libraries it uses keep their own licences, which
are listed in THIRD_PARTY_NOTICES.md. Shank belongs to Klei Entertainment, and this project isn't affiliated with or
endorsed by Klei.
