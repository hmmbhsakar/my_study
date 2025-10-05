---
title: FFmpeg
tags: ["video","audio","content"]
---

## Main Information

> Official Website: [FFmpeg](https://www.ffmpeg.org/)

## Download & Install

### 

### Window
1. By [gyan.dev](https://www.gyan.dev)\
   1. Download Build Link: [FFmpeg Window Binaries](https://www.gyan.dev/ffmpeg/builds/)
   2. Using Package Manager
      1. release essentials: `choco install ffmpeg` Or `winget install "FFmpeg (Essentials Build)"`
      2. release full: `choco install ffmpeg-full` Or `scoop install ffmpeg` Or `winget install ffmpeg`
         1. Single Executable: All FFmpeg components and libraries are compiled into one large ffmpeg.exe file.
         2. Self-Contained: You don't need to distribute separate DLL files alongside the executable.
         3. Larger File Size: The single executable is larger because it includes copies of all necessary library code.
         4. No Runtime Dependencies: No external library files are needed for it to run, simplifying distribution for end-users.
         5. Choose Full (Static) if: You want the simplest deployment where you can just distribute a single ffmpeg.exe file and don't want to worry about missing DLL files. 
      3. release full shared: `scoop install ffmpeg-shared` Or `winget install "FFmpeg (Shared)"`
         1. Multiple DLLs: The main ffmpeg.exe program, along with its various functional libraries (libavcodec, libavformat, etc.), are provided as separate, individual DLL files. 
         2. Smaller Executables: The main FFmpeg program and the individual libraries are smaller in file size compared to a single static executable. 
         3. Runtime Dependency: These DLL files must be present and accessible in the same directory as the ffmpeg.exe for the program to function. 
         4. Memory Efficiency (Potentially): If multiple applications on a system use the same FFmpeg shared libraries, those libraries only need to be loaded into memory once, saving system resources. 
         5. Choose Full-Shared if: You need to use the individual FFmpeg libraries (e.g., with other programs), want to reduce the overall disk space used by FFmpeg, or need to benefit from shared library loading if multiple applications use them. 

## How To

### Merge all/list of audio/video Files in a directory

1. Create a file List: First, create a text file (e.g., mylist.txt) that lists all the files you want to merge, in the desired order. Each line in this file should follow the format `file 'filename.format'`
   1. File List Creations Script for a particular file format
      1. Linux/macOS (using Bash): `for f in *.format; do echo "file '$f'" >> mylist.txt; done`
      2. On Windows 
         1. using Command Prompt: `(for %i in (*.format) do @echo file '%i') > mylist.txt`
         2. Using Powershell: 'Get-ChildItem -Path ".\*.opus" | ForEach-Object { "file '$($_.Name)'" } | Out-File -FilePath "mylist.txt" -Encoding utf8'
2. Merge the files with ffmpeg: `ffmpeg -f concat -safe 0 -i mylist.txt -c copy output.format`
   - -f concat: Specifies the concat demuxer for handling the list of input files.
   - -safe 0: Allows ffmpeg to process potentially unsafe file paths (useful if your filenames contain special characters).
   - -i mylist.txt: Specifies the input file containing the list of desired files to be merged in `file 'filename.format'`.
   - -c copy: Instructs ffmpeg to copy the audio streams directly without re-encoding, which is faster and maintains quality.
   - output.format: The name of the merged output file.

