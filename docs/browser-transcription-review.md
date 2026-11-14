# Browser transcription companion review

Date: 2026-11-14

## Scope

Clarify how the optional Video Digest Whisper fallback works when captions are absent, especially the new browser route and its privacy and security boundaries. This is a documentation update; Source-Weave does not bundle the Video Digest tool, browser runtime, or model files.

## Review criteria

- Preserve captions as the preferred source and transcription as opt-in.
- Distinguish local audio processing from remote runtime/model downloads.
- State machine-generated output and transcript verification limits.
- Avoid recommending that users disable operating-system or organization security controls.
- Keep Source-Weave portable and clear that companion tools are optional.

## Static instruction review

| Case | Existing guidance | Updated guidance | Judgment | Evidence |
| --- | --- | --- | --- | --- |
| Captions are available | Prefer captions; use Whisper only as an explicit fallback | Captions remain preferred; transcription remains opt-in | Preserved | README and skill text |
| Local captions are missing | Local Whisper may create timestamped generated text | Browser route is documented as local inference with loopback-only transcript handoff; runtime/model downloads are disclosed | Clarified | Video Digest implementation review; local browser inference reported 15 timestamped chunks on a 40-second test clip |
| Native PyTorch runtime is blocked | No explicit policy-handling instruction | Do not disable security controls; use an allowed browser route or state the blocker | Improved guidance | User's Windows Application Control blocked torch.dll; browser route completed inference |
| Transcript quality | Model output may omit or hallucinate words | Machine attribution and quote verification remain explicit | Preserved | Existing README and skill caveats retained |

This is a static review of documentation, not a behavioral comparison of Source-Weave. The browser transcript's words were not checked against audio; the new browser-to-file save path was not confirmed end-to-end in that run. No accuracy, speed, or credit savings claim is made.
