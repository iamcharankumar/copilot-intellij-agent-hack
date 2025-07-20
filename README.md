# Turn IntelliJ Into a Context-Aware AI Powerhouse with Claude and MCP

Boost your dev productivity with AI agents powered by Claude + Playwright/Selenium + MCP in IntelliJ like a boss. No,
you won't require Claude desktop this time. 😉

Simple Idea

> The LLMs [Large Language Models] has no decision-making capability.
> So think MCP as your middleware, which use an LLM and talk to you application.
> In this case our application is [Swag Labs](https://www.saucedemo.com/).
> When An LLM is integrated with MCP, we get an AI
> Agent that will help you in decision-making process.

## Prerequisites

Ensure you have the following installed:

1. IntelliJ IDEA (latest)
2. Node.js + npm (LTS)
3. GitHub Copilot IntelliJ Plugin

## Install GitHub Copilot IntelliJ Plugin

![This is a sample image]()

1. Open IntelliJ
2. Navigate to Settings → Plugins
3. Search for GitHub Copilot
4. Click Install
5. Restart IntelliJ

## Authenticate GitHub Copilot

1. After restart, go to File → Settings → Copilot
2. Click **Sign in to GitHub**
3. Follow the OAuth flow in the browser and authorize IntelliJ with your GitHub account account.
4. Once authenticated, Copilot will be active in your IntelliJ editor, suggesting code completions and snippets as you
   type.

## AI Agent Preview: MCP Server Setup

Use the provided config file to run MCP Servers for Playwright and Selenium.

The below json is configured with the
official [Playwright MCP](https://github.com/microsoft/playwright-mcp?tab=readme-ov-file#getting-started) server
and [Angie Jones' Selenium MCP for Claude Desktop](https://github.com/angiejones/mcp-selenium?tab=readme-ov-file#use-with-other-mcp-clients-eg-claude-desktop-etc).

```json
{
  "servers": {
    "playwright": {
      "command": "npx",
      "args": [
        "@playwright/mcp@latest"
      ]
    },
    "selenium": {
      "command": "npx",
      "args": [
        "-y",
        "@angiejones/mcp-selenium"
      ]
    }
  }
}
```

1. Make sure the above json file is named as `mcp.json` and save in the location
   `~/.config/github-copilot/intellij/mcp.json.` The config folder is a hidden folder. So make sure that it is unhidden
   while placing it. Once you completed this step, execute the below command from your terminal.
2. Execute `cat ~/.config/github-copilot/intellij/mcp.json` to see the content of the `mcp.json` file.
3. You should be able to see the mcp.json file content like shown in the below image.
4. Now open your IntelliJ and enter the example prompt to see the MCP + LLM integration.

## What will blow your mind?

The agent analyses login states on its own.
That’s the contextual decision-making in action that will help you
leverage your mundane instruction clarifications everytime.

Ask it for Playwright + TestNG Java 8 code →
It generates production-ready test scripts — literally ready to commit to your feature branch. See in the demo video.