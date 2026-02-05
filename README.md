# Game Build Automation Script

This project is a Python automation tool designed to streamline the management and compilation of Go-based games. It scans a raw data directory, identifies valid game projects, organizes them into a clean workspace, and automatically compiles the source code.

## 🚀 Features

- **Automated Discovery**: Recursively scans directories to find game projects (folders containing "game").
- **Smart Cleaning**: Copies valid projects to a target directory and renames them (removes "_game" suffix).
- **Metadata Generation**: Creates a `metadata.json` file listing all processed games.
- **Auto-Compilation**: Detects `.go` files and runs `go build` to generate executable binaries for each game.
- **Noise Filtering**: Intelligently ignores non-game files and directories (like `a.py`, `info.txt`).

## 🛠️ Prerequisites

- **Python 3.x** (to run the script)
- **Go (Golang)** (to compile the games)

## 💻 Usage

Run the script from the command line by providing the source directory and the target directory:

```bash
python3 get_game_data.py [source_dir] [target_dir]
```

### Example

```bash
python3 get_game_data.py data cleaned_games
```

This command will:
1.  Read game folders from `data/`.
2.  Create a new folder named `cleaned_games/`.
3.  Place the organized and compiled games inside `cleaned_games/`.

## 🎮 Running the Games

After running the script, navigate to the target directory to play the games:

**Hello World:**
```bash
./cleaned_games/hello_world/main
```

**Rock Paper Scissors:**
```bash
./cleaned_games/rock_paper_scissors/code
```

**Simon Says:**
```bash
./cleaned_games/simon_says/file
```

## 📂 Project Structure

- `get_game_data.py`: The main automation script.
- `data/`: Sample directory containing raw game projects and test files.
- `cleaned_games/`: (Generated) The output directory with organized and compiled games.
