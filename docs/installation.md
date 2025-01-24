# Installation Guide

## Prerequisites

- A Spigot/Paper server (1.21+)
- PlaceholderAPI installed on your server

## Step-by-Step Installation

1. **Download PlaceholderAPI**
   - Visit [PlaceholderAPI's Spigot page](https://www.spigotmc.org/resources/placeholderapi.6245/)
   - Download the latest version

2. **Install PlaceholderAPI**
   - Place the PlaceholderAPI.jar in your plugins folder
   - Restart your server
   - Wait for PlaceholderAPI to fully initialize

3. **Install EasyPlaceholders**
   - Download EasyPlaceholders
   - Place the EasyPlaceholders.jar in your plugins folder
   - Restart your server

4. **Verify Installation**
   - Run `/papi info` to verify PlaceholderAPI is working
   - Run `/ep list` to verify EasyPlaceholders is working

## Post-Installation

After installation, a default `config.yml` will be created in the `plugins/EasyPlaceholders` folder. You can:

1. Edit this file to add your custom placeholders
2. Use `/ep reload` to apply changes
3. Test your placeholders using `/papi parse me %easyph_yourplaceholder%`

## Troubleshooting

### Common Issues

1. **Plugin doesn't load**
   - Verify you're using Spigot/Paper 1.21+
   - Check if PlaceholderAPI is installed
   - Check server logs for errors

2. **Commands don't work**
   - Ensure you have the correct permissions
   - Default permission: `easyplaceholders.admin`

3. **Placeholders don't work**
   - Verify the placeholder format: must start with `%easyph_`
   - Check if conditions are correctly formatted
   - Use `/papi parse me` to test placeholders

Need more help? Check our [Support](support.md) page.
