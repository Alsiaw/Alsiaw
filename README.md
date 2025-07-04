<div align="center">

# 🤖 Alsia Discord Bot

### Professional Discord Management Bot for FiveM Servers

[![Discord.js](https://img.shields.io/badge/Discord.js-v14-blue.svg)](https://discord.js.org/)
[![Node.js](https://img.shields.io/badge/Node.js-v16+-green.svg)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Database-green.svg)](https://www.mongodb.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Stars](https://img.shields.io/github/stars/kullaniciadi/alsia-bot?style=social)](https://github.com/kullaniciadi/alsia-bot/stargazers)

**Alsia** is a comprehensive Discord management bot developed specifically for FiveM servers. With advanced moderation system, whitelist management, player statistics, and automated punishment system, it helps you manage your server professionally.

[🚀 Quick Start](#-quick-start) • [📋 Commands](#-command-guide) • [⚙️ Installation](#️-installation) • [📞 Support](#-support)

</div>

---

## 📑 Table of Contents

- [🌟 Features](#-features)
- [📋 Command Guide](#-command-guide)
- [🚀 Quick Start](#-quick-start)
- [⚙️ Installation](#️-installation)
- [🔧 Configuration](#-configuration)
- [🛠️ Technical Details](#️-technical-details)
- [📞 Support](#-support)

---

## 🌟 Features

<table>
<tr>
<td width="50%">

### 🛡️ **Advanced Moderation**
- Comprehensive ban/mute system
- Warning and punishment management
- Automatic penalty reduction
- Evidence-based punishment system

### 📋 **Whitelist Management**
- Player approval/rejection system
- Automatic hex verification
- Blacklist management
- FiveM integration

</td>
<td width="50%">

### 📊 **Statistics System**
- Detailed player and server statistics
- Daily/weekly reports
- Activity tracking
- Ranking systems

### 🔧 **Advanced Features**
- Steam hex management
- Organization system
- Spotify integration
- Automated logging system

</td>
</tr>
</table>

---

## 📋 Command Guide

### 🛡️ Moderation Commands

| Command | Parameters | Permission | Description |
|---------|------------|------------|-------------|
| `/ban` | `player` `reason` | Moderator | Bans a player from the server |
| `/unban` | `ID` `reason` | Moderator | Unbans a player |
| `/forceban` | `ID` `reason` | Admin | Force ban operation |
| `/ban-sorgu` | `ID` | Moderator | Query ban information |
| `/perma` | `player` `issuer` `reason` `evidence` | Admin | Permanent ban |
| `/uyarı` | `player` `issuer` `reason` `evidence` | Moderator | Issue a warning |
| `/uyarı-iptal` | `player` | Moderator | Cancel warning |

### 📋 Whitelist Commands

| Command | Parameters | Permission | Description |
|---------|------------|------------|-------------|
| `/wlceza` | `player` `issuer` `reason` `evidence` | Admin | Issue whitelist punishment |
| `/wlceza-iptal` | `player` | Admin | Cancel WL punishment |
| `/blacklist` | `ID` `hex` `reason` | Admin | Add to blacklist |
| `/blacklist-iptal` | `hex` | Admin | Remove from blacklist |
| `/hex-bul` | `ID` | Moderator | Find player's hex address |
| `/hex-oyuncular` | `hex` | Moderator | List players by hex |

### 👥 Role & Player Management

| Command | Parameters | Permission | Description |
|---------|------------|------------|-------------|
| `/rolver` | `player` `role` | Admin | Give role to player |
| `/rolal` | `player` `role` | Admin | Remove role from player |
| `/rolbilgi` | `role` | Moderator | Get role information |
| `/isim` | `player` `name` | Admin | Change player name |
| `/isimler` | `player` | Moderator | Show player's name history |
| `/seviye` | `player/id` | Everyone | Show player level |

### 📊 Statistics & Information

| Command | Parameters | Permission | Description |
|---------|------------|------------|-------------|
| `/istatistik` | `player` | Moderator | Detailed player statistics |
| `/kayıtlar` | `ID` | Moderator | Show player records |
| `/sicil-sorgu` | `tag-id` | Moderator | Show criminal records |
| `/spotify` | `player/id` | Everyone | Show Spotify status |
| `/top` | `option` | Everyone | Show ranking lists |
| `/topkayıt` | - | Everyone | Top registration makers |
| `/top-kayıt` | - | Everyone | Registration rankings |

### 🏢 Organization Commands

| Command | Parameters | Permission | Description |
|---------|------------|------------|-------------|
| `/oluşum-kur` | `name` `color` `boss` | Admin | Create new organization |
| `/etiket-sorgu` | `#36` | Moderator | Query tag information |

### 🎫 Ticket System

| Command | Parameters | Permission | Description |
|---------|------------|------------|-------------|
| `/ticket-isim` | `name` | Moderator | Change ticket name |
| `/ticket-işlem` | `option` `player` | Moderator | Ticket operations |
| `/ticket-sil` | - | Moderator | Delete ticket |

### 🔧 Server Management

| Command | Parameters | Permission | Description |
|---------|------------|------------|-------------|
| `/sunucu` | `active/maintenance` | Admin | Change server status |
| `/sunucu-veri` | - | Admin | Show server data |
| `/ip` | - | Everyone | Server IP information |
| `/ts3` | - | Everyone | TeamSpeak 3 information |

### 🛠️ Utility Commands

| Command | Parameters | Permission | Description |
|---------|------------|------------|-------------|
| `/sil` | `amount` | Moderator | Delete specified amount of messages |
| `/git` | `staff` | Moderator | Teleport to staff member |
| `/afk` | `reason` | Everyone | Enter AFK mode |
| `/kanal` | `selection` | Admin | Channel operations |
| `/ship` | - | Everyone | Random matching |
| `/sd` | `player` | Everyone | Short player information |
| `/perm-log` | `player` | Admin | Show perm history |
| `/toplu-perm-al` | `role` | Admin | Bulk permission removal |
| `/tweet` | `text` | Admin | Send tweet |

### 🔸 Prefix Commands (.)

| Command | Description |
|---------|-------------|
| `.snipe` | Show last deleted message |

### 🔸 Context Menu Commands (Right Click)

| Command | Description |
|---------|-------------|
| **Whitelist Approve** | Approve player for whitelist |
| **Whitelist Reject** | Reject whitelist application |
| **Ban Player** | Quick ban operation |
| **Add Hex** | Add hex to player |
| **Statistics** | Show player statistics |

---

## 🚀 Quick Start

### Prerequisites

- [Node.js](https://nodejs.org/) (v16 or higher)
- [MongoDB](https://www.mongodb.com/) database
- Discord Bot Token
- FiveM Server (optional)

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/username/alsia-bot.git
   cd alsia-bot
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Configure the Bot**
   - Edit `config.json` file
   - Configure `ayarlar.json` according to your server

4. **Start the Bot**
   ```bash
   node alsia.js
   ```
   or
   ```bash
   npm start
   ```

---

## ⚙️ Installation

### System Requirements

| Component | Requirement |
|-----------|-------------|
| **Node.js** | v16.0.0 or higher |
| **NPM** | v7.0.0 or higher |
| **MongoDB** | v4.4 or higher |
| **Memory** | 512MB RAM minimum |
| **Storage** | 1GB free space |

### Step-by-Step Setup

1. **Download the Project**
   ```bash
   git clone https://github.com/username/alsia-bot.git
   cd alsia-bot
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   Create and configure your environment files:
   - `config.json` - Bot token and database connection
   - `ayarlar.json` - Server-specific settings

4. **Database Setup**
   - Install MongoDB
   - Create a new database
   - Update connection string in `config.json`

5. **Discord Bot Setup**
   - Create a new application on Discord Developer Portal
   - Create a bot and copy the token
   - Invite the bot to your server with necessary permissions

6. **Start the Bot**
   ```bash
   node alsia.js
   ```

---

## 🔧 Configuration

### config.json
```json
{
  "token": "YOUR_BOT_TOKEN_HERE",
  "mongoDB": "YOUR_MONGODB_CONNECTION_STRING_HERE"
}
```

### ayarlar.json
Configure all bot settings in this file:

- **Bot Settings**: Server ID, prefix, status message
- **Permissions**: Command permissions and roles
- **Roles**: Whitelist, staff, and other roles
- **Log Channels**: Log channels for all operations
- **FiveM Settings**: Server information and integration

Fill in all fields in the `ayarlar.json` file for detailed configuration.

### Required Permissions

The bot requires the following Discord permissions:
- `ADMINISTRATOR` (recommended)
- `MANAGE_ROLES`
- `MANAGE_CHANNELS`
- `MANAGE_MESSAGES`
- `BAN_MEMBERS`
- `KICK_MEMBERS`
- `VIEW_AUDIT_LOG`

---

## 🛠️ Technical Details

### Built With

| Technology | Purpose |
|------------|---------|
| **Discord.js v14** | Discord API integration |
| **MongoDB/Mongoose** | Database management |
| **Five.db** | Local data storage |
| **Canvafy** | Image generation |
| **Moment.js** | Date/time operations |
| **Node-cron** | Scheduled tasks |

### Project Structure

```
alsia-bot/
├── alsia.js                 # Main bot file
├── ayarlar.json            # Bot configuration
├── config.json             # Token and DB settings
├── package.json            # Project dependencies
├── alsia/
│   ├── eventler/           # Bot events
│   └── komutlar/           # Command files
│       ├── Slash/          # Slash commands
│       ├── Prefix/         # Prefix commands
│       └── SağTık/         # Context menu commands
├── database/               # Database models
└── croxydb/               # Local data files
```

### Feature Details

#### Moderation System
- Automatic penalty reduction system
- Detailed logging
- Evidence-based punishment system
- Time-based penalty management

#### Whitelist System
- Automatic hex verification
- Blacklist management
- Player approval/rejection system
- FiveM integration

#### Statistics System
- Message and voice statistics
- Daily/weekly reports
- Player activity tracking
- Ranking lists

---

## 📊 API Integration

### FiveM Integration
The bot can integrate with FiveM servers to:
- Sync player data
- Manage server whitelist
- Track player activity
- Automated punishment system

### Database Schema
```javascript
// Player Schema Example
{
  discordId: String,
  steamHex: String,
  whitelistStatus: Boolean,
  punishments: Array,
  statistics: Object,
  registrationDate: Date
}
```

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines

- Follow ESLint configuration
- Write clear commit messages
- Test your changes thoroughly
- Update documentation as needed

---

## 📞 Support

If you encounter any issues or have suggestions:

- **Discord**: alsiaw
- **GitHub Issues**: [Create an issue](https://github.com/username/alsia-bot/issues)
- **Documentation**: [Wiki](https://github.com/username/alsia-bot/wiki)

### Common Issues

| Issue | Solution |
|-------|----------|
| Bot not responding | Check token and permissions |
| Database connection error | Verify MongoDB connection string |
| Commands not working | Ensure proper role permissions |

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🏆 Acknowledgments

- Discord.js community for excellent documentation
- FiveM community for inspiration
- All contributors who helped improve this project

## 👨‍💻 Developer

**Alsia** - *FiveM Discord Bot Developer*

---

<div align="center">

⭐ **If you like this project, please give it a star!**

[![GitHub stars](https://img.shields.io/github/stars/username/alsia-bot?style=social)](https://github.com/username/alsia-bot/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/username/alsia-bot?style=social)](https://github.com/username/alsia-bot/network)

</div>
