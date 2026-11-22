# Audio to MIDI Converter — MP3, WAV to MIDI Notes & Key — MCP Server

Convert songs, recordings and stems to MIDI from your AI agent or MCP client, with Spotify Basic Pitch polyphonic transcription — piano, guitar, bass, vocals, any instrument. Send a public MP3, WAV, FLAC, M4A or MP4 URL and get a .mid file, the note list (pitch, timing, velocity), tempo, key and pitch range.

This repo is the MCP listing for the [Audio to MIDI Converter — MP3, WAV to MIDI Notes & Key](https://apify.com/magnova/audio-to-midi-converter) Actor by Magnova on Apify. The server is hosted by Apify at the pinned endpoint below — there is nothing to install or run from this repository; you just point your MCP client at the URL.

## Tools

The pinned connection loads a focused tool set:

- **magnova--audio-to-midi-converter** — Convert a public audio URL (MP3, WAV, FLAC, M4A or MP4) to MIDI. Returns a .mid file plus the note list (pitch, timing, velocity), tempo, key and pitch range.
- **fetch-actor-details** — Fetch the Actor's full input schema, pricing, and documentation, so an agent can check parameters and cost before running it.
- **get-actor-run / get-dataset-items** — Run and storage helpers, loaded automatically, used to fetch the results a run produced.

## Connect

Pinned endpoint (Streamable HTTP):

```
https://mcp.apify.com?tools=fetch-actor-details,magnova/audio-to-midi-converter
```

On first connect, your client will ask you to sign in with your Apify account (OAuth). If your client cannot do OAuth, pass your Apify API token as an `Authorization: Bearer <YOUR_APIFY_TOKEN>` header instead.

### Cursor / VS Code / other Streamable HTTP clients

```json
{
  "mcpServers": {
    "audio-to-midi-converter": {
      "url": "https://mcp.apify.com?tools=fetch-actor-details,magnova/audio-to-midi-converter"
    }
  }
}
```

### Claude Desktop

Claude Desktop's config file only runs local commands, so use the `mcp-remote` bridge:

```json
{
  "mcpServers": {
    "audio-to-midi-converter": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.apify.com?tools=fetch-actor-details,magnova/audio-to-midi-converter"
      ]
    }
  }
}
```

The same pinned URL also lives in this repo's `.mcp.json`, and `server.json` is the listing for the Official MCP Registry, published as `io.github.memeanalyst/audio-to-midi-converter-mcp`.

## Pricing

Pay per event, billed to your own Apify account: **$0.01 per audio minute, rounded up — failed, silent or undecodable files are free**. No start fee, no subscription, and you are only charged for records actually delivered.

## Links

- Actor on Apify Store: https://apify.com/magnova/audio-to-midi-converter
- MCP endpoint: https://mcp.apify.com?tools=fetch-actor-details,magnova/audio-to-midi-converter

*Conversion runs on the audio you link to; send a public audio URL.*
