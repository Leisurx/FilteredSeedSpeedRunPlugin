# FilteredSeedSpeedrun Plugin

A Minecraft 1.16.1 Spigot plugin for filtered seed speedrunning practice using the [filteredseed.com](https://filteredseed.com) API.

## Features

 **FSG-Style Filtering** - Uses filteredseed.com's verified seed database  
 **Built-in Timer** - Automatic speedrun timer with scoreboard display  
 **Solo & Co-op Modes** - Practice alone or with friends  
 **Automatic Completion Detection** - Timer stops when entering End portal  
 **Multiple Filter Types** - Village, Buried Treasure, Temple, Shipwreck, Ruined Portal, and more  
 **Isolated Worlds** - Each speedrun gets its own Overworld, Nether, and End  
 **Clean Cleanup** - Worlds automatically deleted when finished

## Requirements

- **Minecraft Version**: 1.16.1
- **Server Software**: Spigot or Paper 1.16.1
- **Java**: Java 8 or higher
- **Internet Connection**: Required to fetch seeds from filteredseed.com

## Installation

1. Download `FilteredSeedSpeedrun-1.0.0.jar` from releases
2. Place it in your server's `plugins/` folder
3. Start or restart your server
4. Plugin will load and connect to filteredseed.com

## Commands

| Command | Description | Example |
|---------|-------------|---------|
| `/fsspeedrun help` | Show help menu | `/fsspeedrun help` |
| `/fsspeedrun start <filter>` | Start solo speedrun | `/fsspeedrun start village` |
| `/fsspeedrun start <filter> coop` | Start co-op speedrun | `/fsspeedrun start bt coop` |
| `/fsspeedrun join <player>` | Join co-op speedrun | `/fsspeedrun join Steve` |
| `/fsspeedrun leave` | End/leave speedrun | `/fsspeedrun leave` |
| `/fsspeedrun filters` | List available filters | `/fsspeedrun filters` |

**Aliases**: `/fssr`, `/fsrun`

## Available Filters

| Filter Code | Description |
|-------------|-------------|
| `bt` | Buried Treasure |
| `btop` | Buried Treasure (Overpowered) |
| `village` | Village near spawn |
| `villageop` | Village (Overpowered) |
| `temple` | Desert Temple |
| `templeop` | Temple (Overpowered) |
| `ship` | Shipwreck |
| `shipop` | Shipwreck (Overpowered) |
| `rp` | Ruined Portal |

## How It Works

1. **Start a speedrun**: ex. `/fsspeedrun start village`
2. Plugin fetches a verified seed from filteredseed.com
3. Creates 3 new worlds: Overworld, Nether, End (all with same seed)
4. Teleports you to spawn with a 5-second countdown
5. **Timer starts** and displays on sidebar scoreboard
6. Complete the game as normal

## Co-op Mode

Want to practice with friends?

1. Host starts: `/fsspeedrun start village coop`
2. Friends join: `/fsspeedrun join <host_name>`
3. Everyone spawns in the same world
4. First person to enter the End portal completes the run
5. Timer shows completion for all participants

## Timer Display



## Permissions

| Permission | Description | Default |
|------------|-------------|---------|
| `filteredseed.use` | Use plugin commands | `true` (everyone) |
| `filteredseed.admin` | Admin commands | `op` only |

## Configuration

No configuration needed! The plugin works out of the box by connecting to filteredseed.com's API.

## Troubleshooting

**"Failed to get seed from API"**
- Check your internet connection
- Verify filteredseed.com is accessible
- Try a different filter type

**Worlds not cleaning up**
- Use `/fsspeedrun leave` to manually cleanup
- Restart server to force cleanup all worlds

## Credits

- **Seed Database**: [filteredseed.com](https://filteredseed.com) by AndyNovo
- **Inspiration**: FSG Mod by DuncanRuns and the MCSR community
- **Plugin Developer**: Leisurx


## Version History

### v1.0.0 (2026-01-06)
- Initial release
- FSG filter integration with filteredseed.com
- Built-in speedrun timer
- Solo and co-op modes
- Automatic completion detection
- World isolation and cleanup
