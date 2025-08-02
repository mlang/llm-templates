# LLM Templates

Reusable prompts I've found useful, packaged up as templates for the [llm](https://github.com/simonw/llm) CLI.

To use these, you need the `llm-templates-github` plugin installed:

```bash
llm install llm-templates-github
```

Now you can make use of the templates here, without copying them manually:

## Announce the upcoming song

```bash
mpc queued | llm -t gh:mlang/mpd -p date "$(date)" -p prev "$(mpc current)"
```

## Chat in study mode

```bash
llm chat -t gh:mlang/study
```

## Instruct a TTS how and what to speak

```bash
llm -t gh:mlang/tts "A short poem" | llm tts --json
```
