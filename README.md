# Multimedia Claude

**Give Claude a video. Get back finished reels. Zero technical skill required.**

Multimedia Claude turns Claude Code into an autonomous media assistant that actually does the work instead of teaching you how to do it. Drop a sermon recording, a podcast episode, or any video — Claude transcribes it, finds the best moments, cuts the clips, adds captions, adds music, and exports ready-to-post reels. Your only job is to approve the output.

> **This is not a tutorial tool.** Claude won't tell you to open CapCut or download Clipchamp. Claude IS the editor.

## Who This Is For

- Church admins who need sermon reels every week
- Small business owners who want social content from their videos
- Podcasters who want short clips for social
- Anyone who has video content and needs it cut into shareable pieces
- **People who have never opened a terminal before** — that's fine, we got you

## Setup (5 minutes, one time)

### 1. Sign up for Claude Pro ($20/month)
Go to **[claude.ai](https://claude.ai)** → Create account → Upgrade to Pro.

### 2. Open a new chat on claude.ai and paste this:

```
I need you to help me set up Claude Code on my computer so I can use it as my media assistant. I want to give it a sermon video (or any video) and have it automatically make reels for me.

Here's the setup file: https://github.com/chriskjrostad/multimedia-claude/blob/main/CLAUDE.md

I might not have anything installed yet. Don't tell me to figure things out — install everything for me step by step. Ask me what kind of computer I have first. If something goes wrong, fix it before moving on. I am not technical and that's okay.
```

### 3. Follow along. Claude sets everything up for you.

### 4. Once it's running, just say:
```
Here's this week's sermon — make me 5 reels
```

Drop the file in. Claude handles everything else. That's it. You're done.

## What Claude Does With Your Video

1. **Transcribes** the entire recording
2. **Finds the 5 best moments** — self-contained, impactful, 15-45 seconds each
3. **Cuts the clips** — vertical 9:16 format, ready for Reels/Shorts/TikTok
4. **Adds captions** — large, readable, burned into the video
5. **Adds background music** — if you put music files in a `music/` folder
6. **Saves to your Desktop** — or wherever you want them
7. **Asks if you want to post** — can draft captions and post to your social accounts

## What Else Claude Can Do

- **Social media graphics** — "Make me a quote graphic from this verse"
- **Post scheduling** — "Post this to our Facebook page Tuesday at 9am"
- **Content calendar** — "What have we posted this week? What's coming up?"
- **Event graphics** — "Make a graphic for our potluck this Saturday"

## Background Music

Create a `music/` folder and drop in some royalty-free tracks you like. Claude picks one that matches the mood of each clip automatically. No music folder? Claude makes the reels without music and lets you know.

Good free sources for worship/background music:
- [YouTube Audio Library](https://studio.youtube.com/channel/audio) (free for any use)
- [Pixabay Music](https://pixabay.com/music/) (free, no attribution required)

## What It Costs

- **Claude Pro: $20/month** — required, this is the AI that does the work
- **Everything else: free** — ffmpeg, whisper, and all the tools Claude installs are open source

## FAQ

**Do I need to know how to code?**
No. You need to install Claude Code (one command) and then talk to it like a person.

**Do I need to learn ffmpeg or video editing?**
No. Claude uses these tools behind the scenes. You never see them.

**Can Claude actually post to my Facebook/Instagram?**
It can draft posts and save them. To auto-publish, you'd need to connect your social accounts — Claude will walk you through that if you ask.

**What if something goes wrong?**
Tell Claude what happened. Paste the error. It'll fix it. That's what it does.

**Can I use this for things other than sermons?**
Yes — any video or audio content. Podcasts, webinars, talks, interviews, events.

---

Built by [Chris Kjorstad](https://www.linkedin.com/in/chriskjorstad/) — the same person who built [Claude Council](https://github.com/chriskjrostad/claude-council), an AI development operating system used to ship production software with zero human engineers.

## License

MIT — use it, share it, adapt it.
