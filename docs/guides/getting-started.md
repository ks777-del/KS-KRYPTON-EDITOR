# Getting Started with KS KRYPTON VIDEO EDITOR

Welcome to **KS KRYPTON VIDEO EDITOR**! This guide covers the essential workflow for creating your first video project, utilizing the multi-track timeline, leveraging the integrated AI assistant, and rendering your final export.

---

## 1. Creating Your First Project

1. Launch **KS KRYPTON EDITOR** from your desktop or application menu.
2. The **Quick Setup Dialog** will appear:
   - **Project Aspect Ratio:** Select from:
     - `16:9 Widescreen (1920x1080)` (Standard YouTube / TV)
     - `9:16 Vertical / Shorts (1080x1920)` (TikTok, Instagram Reels, YouTube Shorts)
     - `1:1 Square / Social (1080x1080)` (Instagram feed)
     - `16:9 4K UHD (3840x2160)` (Cinematic high resolution)
   - Click **Create New Project**.
3. The main workspace will open with your timeline calibrated to your chosen resolution and frame rate.

---

## 2. Importing Media

There are three ways to import media into your project:
1. **Drag and Drop:** Drag video files, audio tracks, and images from your operating system's file manager directly into the **Project Bin** (top-left dock).
2. **KRYPTON Asset Browser:** Use the dedicated **Asset Browser** dock to navigate your media libraries, sound effects, and title templates.
3. **Menu Option:** Select **Project > Add Clip or Folder…** (or press `Ctrl+Shift+A`).

---

## 3. Timeline Editing Essentials

### Timeline Navigation
- **Playhead:** Drag the playhead cursor along the timeline ruler to scrub through your edit.
- **Playback Controls:** Press `Space` to play/pause. Use `J`, `K`, and `L` for shuttle controls (reverse, stop, fast-forward).
- **Zooming:** Hold `Ctrl` and use the mouse wheel to zoom the timeline scale in or out.

### Cutting and Trimming
- **Razor Tool (`X`):** Click on any clip on the timeline to perform a clean razor cut at the cursor position.
- **Selection Tool (`S`):** Move, trim edges, or reorder clips on tracks.
- **Ripple Delete (`Shift+Del`):** Delete a clip and automatically close the gap by pulling subsequent clips forward.

---

## 4. Using the KS KRYPTON AI Assistant

The **KS KRYPTON AI** workspace panel connects directly to your **Nexus AI Gateway** to perform conversational editing operations.

### Connecting to Nexus
1. In the AI panel header, click **⚙ Settings**.
2. Verify the gateway endpoint (`http://localhost:20128/v1`).
3. Click **↻ Refresh** to populate all available models, then click **Connect / Save**.
4. The status badge will show **● Connected**.

### Common AI Editing Directives
- **Split & Scene Detection:**
  > *"Analyze the selected clip on Video 1 and split at every scene transition."*
- **Audio Cleanup & Silence Removal:**
  > *"Detect all pauses longer than 1 second in the voiceover track and ripple delete the silent sections."*
- **Pacing & Montage Assembly:**
  > *"Arrange the imported B-roll clips to match the tempo of the music track on Audio 2."*

---

## 5. Exporting & Rendering Your Video

1. When your edit is complete, click **Export / Render** in the top header toolbar (or press `Ctrl+Enter`).
2. Select your export profile:
   - **MP4 / H.264 (Default):** Universal playback across web, mobile, and television.
   - **H.265 / HEVC:** High-efficiency compression for 4K workflows.
   - **Apple ProRes / DNxHR:** Lossless intermediate codecs for color grading.
3. Choose your destination file path and click **Render to File**.
4. A progress monitor will show the rendering job status and notify you upon completion.
