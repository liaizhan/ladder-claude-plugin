# Ladder by Aizhan Li

The Ladder self-check by Aizhan Li, author of the Ladder method, as a plugin for Claude. Name a goal you can measure, say where you are now, list the obstacles between you and the goal and the fears above it. Claude arranges your answers into a ladder and gives a short reading: which obstacle stands closest to you, what the ladder shows, and two questions to think about.

Works in Russian, Kazakh and English. Free. It does not diagnose and does not replace a doctor or a psychologist.

## What is inside

- **Skill `ladder-self-check`**: tells Claude how to run the self-check: questions one at a time, the person's own words, a careful answer when someone is in crisis.
- **Command `/ladder-by-aizhan-li:start`**: starts the self-check in Claude Code and Cowork. In chat, just ask Claude to do the Ladder self-check.
- **Connector `ladder`**: the read-only MCP server at `https://108psy.com/mcp`, no sign-in. Two tools: `get_ladder_questions` returns the questions, `analyze_ladder` reads the ladder by the rules of the method. No AI model runs on the server.

## Use it

In Claude Code:

```
/plugin marketplace add liaizhan/ladder-claude-plugin
/plugin install ladder-by-aizhan-li@ladder-by-aizhan-li
```

On claude.ai, add the plugin, connect the Ladder connector on the plugin's Connectors tab, and write "Let's do the Ladder self-check" (or «Давай пройдём Лестницу»).

## Data

When you answer, Claude sends your short answers (the goal, the "I" step, the obstacles and the fears) and the language code to `https://108psy.com/mcp`. The server reads them, returns the reading and keeps nothing: answers are not stored and not written to logs. No name, email or phone number is asked for or sent. The plugin sends nothing anywhere else.

Do not enter diagnoses, symptoms or medication: the tools do not analyze health details. If the words show signs of crisis or violence, the server returns helpline numbers instead of a reading.

Privacy policy: <https://108psy.com/en/privacy>

Help: <https://108psy.com/pomosh>

## Author

Aizhan Li, author of the Ladder method, Kazakhstan. https://108psy.com/ob-avtore

## License

MIT, see [LICENSE](LICENSE).
