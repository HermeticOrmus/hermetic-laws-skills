# Using this repo with Cursor

This project includes a Cursor project rule that loads the Hermetic framings as context.

## In this repository

1. Open the folder in Cursor.
2. The rule [`.cursor/rules/hermetic-laws.mdc`](.cursor/rules/hermetic-laws.mdc) is committed with `alwaysApply: false` (it's contextual, not always-on).
3. Confirm under **Settings → Rules**.

## Use the same framings in another project

**Cursor**: Copy `.cursor/rules/hermetic-laws.mdc` into that project's `.cursor/rules/`.

**Other AI tools**: Copy [`CLAUDE.md`](CLAUDE.md) to the project root.

## On `alwaysApply`

I set `alwaysApply: false` because these principles work best as on-demand framings, not as constant background noise. Invoke them when:

- Architecture feels unclear → Mentalism
- Layers feel disconnected → Correspondence
- Can't ship → Vibration
- Decision is binary but both options are wrong → Polarity
- Team / you are burning out → Rhythm
- Same bug recurring → Cause and Effect
- System dead or imbalanced → Gender

If you'd rather have them always-on, change to `alwaysApply: true`.
