# AudioExtractor

AudioExtractor is a lightweight Windows shell extension that adds an **"Extract Audio (MP3)"** option to your right-click context menu in Windows Explorer. It allows you to quickly strip audio from video files or convert other audio formats to high-quality MP3 (192kbps) without opening a heavy media converter.

## 🚀 Features

- **Explorer Integration**: Native right-click context menu entry.
- **Smart Filtering**: Only shows up for supported media files (MP4, MKV, AVI, MOV, MP3, WAV, M4A, FLV, WEBM).
- **High Quality**: Uses FFmpeg with `libmp3lame` at 192kbps for crystal-clear audio.
- **Automated Installer**: A dedicated GUI installer that handles everything for you.
- **No Manual Setup**: The installer automatically downloads and configures FFmpeg and the necessary DLLs.

## 🛠️ Installation

1. Download the latest `AudioExtractorInstaller.exe` from the [Releases](../../releases) page.
2. Right-click the installer and select **Run as Administrator** (required to install files to `System32` and register the shell extension).
3. Click **Install Now**.
4. Once completed, you'll see a success message. You're ready to go!

## 📖 How to Use

1. Open Windows Explorer and find a video or audio file.
2. **Right-click** the file.
3. Select **"Extract Audio (MP3)"**.
4. A command-less FFmpeg process will run in the background.
5. Once finished, a new file named `filename_audio.mp3` will appear in the same folder.

## ⚙️ Technical Details

- **Language**: C++ (Win32 API / COM)
- **Backend**: FFmpeg CLI
- **Shell Extension**: Implements `IShellExtInit` and `IContextMenu`.
- **Installer**: Native Win32 GUI using `WinINet` for automated dependency fetching.

## 📜 License

FFmpeg is a trademark of Fabrice Bellard, originator of the FFmpeg project.
