# OpenAI Direct Codex API Channel Report

- status: prepared_not_enabled
- API key included: no
- source code included: no
- DWG/DXF/PDF/image/customer data included: no
- OpenAI request body included: no
- OpenAI decision JSON included: no
- direct execution of AI-returned commands: blocked

## Safe Summary

The private repository now contains a prepared OpenAI Responses API decision channel for the Windows guardian.

The channel is dry-run only and not connected to the 10-minute guardian loop.

If `OPENAI_API_KEY` or `OPENAI_MODEL` is missing on Windows, the scripts write reports and skip the API call.

The AI output is advisory only. The guarded apply step writes a report, blocks high-risk decisions, and never executes model-returned shell commands automatically.

## Next Recommendation

Run the dry-run pipeline on Windows first. If approved later, call the API at most hourly, not every 10 minutes.
