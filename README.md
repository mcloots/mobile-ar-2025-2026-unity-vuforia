# Project openen

- Start Unity Hub, kies exact de Unity-versie die dit project gebruikt (LTS aangeraden).
- Open de map van dit repo als Unity project.
- Wacht tot alle assets en packages klaar zijn met importeren.

# Vuforia configureren

- Installeer Vuforia package voor Unity
- Open de hoofdpagina/scene (bijv. Assets/Scenes/Main.unity).
- In de Scene staat een Vuforia ARCamera.
- Voeg je Vuforia License Key toe
- Importeer Vuforia target database indien nodig

# Buildinstellingen (belangrijk)

Ga naar Project Settings → Player → Android → Other Settings:

- Scripting Backend: IL2CPP
- Target Architectures: ✔ ARM64 en ✖ ARMv7 (Vuforia ondersteunt geen ARMv7)
- Auto Graphics API: uit
- Graphics API: OpenGLES3 (zet Vulkan uit)

# Exporteren voor Flutter (plugin-menu)

- Installeer indien nodig de unity package voor flutter_embed_unity
- In het menu: Flutter Embed → Export project to Flutter app (Android)
- Select folder: <pad-naar-flutter-app>/android/unityLibrary
