# rain-journal

English | [日本語](README.ja.md)

An agent skill that records negative feelings as rain, then lets you reread them gently after the rain to turn them into small improvements

The skill replies in the language you write in

## Install

With skills

```sh
npx skills add https://github.com/sayuprc/rain-journal
```

With APM

```sh
apm install https://github.com/sayuprc/rain-journal
```

Manually: copy `skills/rain-journal` into your agent's skills directory

Agents that don't support `disable-model-invocation` may invoke the skill automatically

## Usage

- Record the rain: invoke `rain-journal` and write what's weighing on you (e.g. "I couldn't say anything in today's meeting. I'm always like this")
- Reread after the rain: ask to look back (e.g. "I want to look back on recent days")

Once invoked, the skill enters shelter mode (雨宿りモード), so you can keep talking without invoking it again

Shelter mode ends when you say something like "done" or "exit" (「終わり」「解除」), or when the session ends

## Terms

- **Rain (雨)**: negative thoughts and feelings you let out
- **Break in the clouds (晴れ間)**: signs that the rain has lessened or softened
- **Umbrella (傘)**: light advice to prepare for the next rain

## Records

Records are saved as Markdown in `~/.rain-journal/`

- `<datetime>.md`: the rain recorded during one shelter mode session
- Chosen umbrellas are kept in `umbrellas` of the rain record they answer
