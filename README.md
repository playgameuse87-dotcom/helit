# helit
Ludo Classique
Ludo Dream - Unity Local Clone (scaffold)

What's inside:
- Assets/Scripts/: main C# scripts for the offline/local Ludo Dream clone
- Assets/Editor/BuildScriptAndroidSigned.cs : Editor build helper for Android
- Assets/Scenes/: create Main.unity here
- Prefabs/Models/Audio: add your assets

How to use:
1) Download and unzip this folder.
2) Open Unity (2021.3 LTS or 2022.3 LTS recommended).
3) Open the folder as a project or copy Assets/ into a new Unity project.
4) Create Assets/Scenes/Main.unity (Scene) and add GameObjects:
   - GameManager (attach GameManager)
   - BoardManager (attach BoardManager and set 52 track transforms)
   - BoardLogic (attach BoardLogic)
   - UIManager (attach UIManager and wire UI refs)
   - Dice (attach Dice and AudioSource)
   - Create Player prefabs or place PlayerController objects in the scene and set pawnBasePositions
5) Create Pawn prefab (mesh + PawnController + Animator).
6) Assign track transforms and home transforms in BoardManager.
7) Add audio files in Assets/Audio and 3D models in Assets/Models.
8) Use Build > Build Android APK/AAB (the Editor script will set IL2CPP + ARM64). For signed builds set environment variables or put a keystore at project root.

Notes:
- BoardLogic implements core rules (enter on 6, capture, house entry, overshoot prevention).
- This scaffold contains code but no binary assets (models/sounds). Use Kenney / OpenGameArt for free assets.
- If you want, I can also produce a ZIP including recommended free assets (models + sounds). Ask for assets pack.

Enjoy building Ludo Dream!
