# Animate Bone Tools

[![Blender](https://img.shields.io/badge/Blender-3.6%2B-orange)](https://www.blender.org/)
[![License](https://img.shields.io/badge/License-GPL%203.0-blue)](LICENSE)


![Animate Bone Tools Interface](screenshots/Painel_Animate_Bone_Toos.png.png)
**Animate Bone Tools** is an addon for Blender that streamlines character animation workflow by providing quick access to bone reset, rotation controls, pose mirroring, and keyframe insertion - all in one convenient panel.

## ✨ Features

- **Reset Bones** - Reset location, rotation, and scale of selected bones (Alt+G + Alt+R + Alt+S combined)
- **Rotation Controls** - Rotate bones on X, Y, Z axes with adjustable angle (0.1° to 45°)
- **Mirror Pose** - Quickly mirror the pose of selected bones across the X axis
- **Insert Keyframe** - Insert keyframes for location, rotation, and scale with one click

## 📋 Requirements

- Blender 3.6 or higher
- Armature in Pose Mode

## 🚀 Installation

1. Download `animate_bone_tools.py`
2. Open Blender
3. Go to `Edit > Preferences > Add-ons`
4. Click `Install...` and select the downloaded file
5. Enable **"Animation: Animate Bone Tools"**
6. Find the panel in the 3D Viewport sidebar (press `N`)

## 🎮 Usage

### Quick Start

1. Select your armature
2. Enter **Pose Mode** (`Ctrl + Tab` → Pose Mode)
3. Select one or more bones
4. Open the sidebar (`N`) and go to the **Bone Tools** tab


### Features in Detail

#### 🔄 Reset Bones
- Resets **location** to (0,0,0)
- Resets **rotation** to identity (0°)
- Resets **scale** to (1,1,1)
- Works with all rotation modes (Quaternion, Euler, Axis Angle)

#### 🎛️ Rotation Controls
- Rotate bones in **5° increments** (configurable)
- Independent control for **X, Y, and Z** axes
- Visual feedback with direction arrows
- Supports all rotation modes automatically

#### 🔀 Mirror Pose
- Copies and flips pose from selected bones
- Perfect for symmetrical characters
- Uses Blender's native mirror system
- Works with any armature orientation

#### 📷 Insert Keyframe
- Inserts keyframes for all transform properties
- Includes location, rotation, and scale
- Groups keyframes by bone name in the Dope Sheet
- Uses current frame position

## 🎯 Supported Rig Types

- ✅ Mixamo
- ✅ Rigify
- ✅ Auto-Rig Pro
- ✅ Custom Armatures
- ✅ Any bone-based rig

## 🛠️ Technical Details

- **Rotation Mode Support**: Quaternion, Euler (all orders), Axis Angle
- **Undo Support**: Full undo/redo for all operations
- **Performance**: Optimized for real-time feedback
- **Compatibility**: Blender 3.6+

## 📖 Keyboard Shortcuts

While no custom shortcuts are assigned by default, you can create your own in Blender's Keymap preferences for these operators:

- `bone.reset_selected_bones` - Reset bones
- `bone.mirror_pose` - Mirror pose
- `bone.insert_keyframe` - Insert keyframe

## ❓ Troubleshooting

### "Select an armature first"
- Make sure you have an armature selected
- Enter Pose Mode before using the tools

### "Select some bones"
- You need to select at least one bone in Pose Mode
- Use `A` to select all bones or `B` for box select

### Rotation doesn't work
- Check if the bone is constrained
- Some rigs have locked transforms
- Try resetting before rotating

### Mirror doesn't work as expected
- Ensure your armature is properly named (e.g., "hand.L"/"hand.R")
- Blender uses bone names with .L/.R suffixes for mirroring

## 🔧 Development

### File Structure

animate_bone_tools.py
├── bl_info (metadata)
├── Operators
│ ├── BONE_OT_reset_selected_bones
│ ├── BONE_OT_rotate_bone
│ ├── BONE_OT_mirror_pose
│ └── BONE_OT_insert_keyframe
└── Panel (BONE_PT_panel)


### Register/Unregister
The addon follows Blender's standard register/unregister pattern and cleans up all properties on uninstallation.

## 📝 Changelog

### Version 1.9
- Added Mirror Pose functionality
- Renamed to "Animate Bone Tools"
- Updated author information
- Improved panel layout

### Version 1.8
- Added Insert Keyframe button
- Removed redundant Wrist Rotation
- Cleaned up interface

### Version 1.0
- Initial release
- Basic reset and rotation controls

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

## 📧 Support

- **Author**: Sergio ReOli
- **Contact**: sergioreoli@hotmail.com
- **PayPal**: [Donate](https://paypal.me/sergioreoli@hotmail.com)

## 📄 License

This project is licensed under the GPL 3.0 License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Blender Foundation for the amazing API
- Mixamo and Rigify communities for inspiration
- All beta testers and contributors

---

**Made with ❤️ for the Blender community**

### Panel Overview
