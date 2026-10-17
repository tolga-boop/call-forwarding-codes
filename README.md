# Call forwarding codes (US and Canada)

How to send the calls you don't answer to another number, by carrier and phone system: the dial codes for mobile carriers and landlines, and the menu path for VoIP systems. Useful for after-hours answering, a receptionist service, or a second phone. Replace `[number]` with the 10-digit destination number, no spaces.

Machine-readable copy: [`codes.json`](codes.json). Kept by [Odile Labs](https://odilelabs.com/forwarding); checked October 2026. VoIP steps come from each provider's own help pages, read 12 October 2026.

## Mobile carriers

| Carrier | No answer | Busy | Phone off / no signal | All calls | Cancel |
|---|---|---|---|---|---|
| AT&T (US) | `**61*+1[number]**10#` | `**67*+1[number]#` | `**62*+1[number]#` | `**21*+1[number]#` | `##61#`, `##67#`, `##62#`, `##21#` |
| T-Mobile (US) | `**61*+1[number]**10#` | `**67*+1[number]#` | `**62*+1[number]#` | `**21*+1[number]#` | `##61#`, `##67#`, `##62#`, `##21#` |
| Verizon (US) | `*71[number]` | `*71[number]` | – | `*72[number]` | `*73` |
| Mint Mobile (US) | `**61*1[number]#` | – | – | – | `##61#` |
| Visible (US) | not possible | – | – | – | – |
| Google Fi (US) | not possible | – | – | – | – |
| Rogers, Bell, Telus (mobile) (CA) | `**61*+1[number]**10#` | – | – | – | – |

Notes:
- **AT&T:** The 10 in the no-answer code is the ring time in seconds; without it the carrier waits about 20 seconds.
- **T-Mobile:** Same codes as AT&T.
- **Verizon:** `*71` covers no answer and busy; it rings 3 to 6 times first and Verizon has no shorter setting. On an iPhone, turn off Live Voicemail first (Settings, Apps, Phone, Live Voicemail): Verizon says it stops `*71` from working.
- **Visible:** Visible's `*71` forwards only while you're on another call; it cannot forward only unanswered calls.
- **Google Fi:** No forwarding for unanswered calls.
- **Rogers, Bell, Telus (mobile):** Try the AT&T codes; if they are refused, the carrier's support sets it.

## Landlines

| Provider | No answer | Cancel | Notes |
|---|---|---|---|
| AT&T or Verizon Fios landline (US) | `*92[number]` | `*93`, `*91` | Busy: `*90[number]`. |
| Rogers home phone (CA) | `*92[number]` | `*93` | Stay on the line 5 seconds; it forwards after 4 rings. With Rogers voicemail on, ask Rogers to switch it. |
| Telus home phone (CA) | `*92[number]` | `*93` | `*94` sets 2 to 9 rings. On newer Telus accounts, Telus sets the number for you. |
| Bell home phone (CA) | ask the provider | – | Ask Bell. |

## VoIP and office phone systems

- **RingCentral:** App: Settings, Phone, Call handling, Edit, Work hours (and After hours), Missed calls, Forward to external number.
- **Google Voice for Workspace:** Admin console, the ring group, Configuration, Unanswered calls, Forward the caller, then the number. Forwards after 30 seconds.
- **Google Voice (personal):** not possible. Cannot forward only missed calls; linked numbers all ring at once.
- **Vonage Business:** Admin Portal, Phone System, Extensions, edit the extension, Call Forwarding, Follow Me: your extension first, then the number.
- **Nextiva:** Voice portal, Users, the user, Actions, Voice Settings, Forwarding, Call forwarding (unanswered): the number and the rings. Admins only; covers direct calls, not call groups.
- **Zoom Phone:** Settings, Phone, Voicemail and forwarding, When a call goes unanswered, Forward to External Contacts. Add the number as an external contact first; an admin may need to allow forwarding outside Zoom.
- **Quo (formerly OpenPhone):** In the number's call flow: a Ring users step, then Forward call to the number, then Publish.
- **8x8:** Admin Console, Users, the user, Call forwarding rules, When user does not answer, Forward directly to a custom number.
- **Microsoft Teams Phone:** Settings, Calls, Call handling and forwarding, If unanswered: the number and the ring time in seconds.
- **3CX:** Web client, Settings, Call Forwarding, Unanswered calls, External number, with the seconds. Calls through a ring group or queue skip these personal rules.
- **Ooma Office:** not possible. Cannot send only unanswered calls to an outside number.

Anything else (Grasshopper, Dialpad, GoTo, Spectrum, Comcast and the rest): ask the provider for "forward on no answer" to the number.

## Check it worked

Call the line from another phone and let it ring; after a few rings the forwarded number should answer.

## Corrections

Carriers change codes. Open an issue or a pull request with the provider's help page as the source.

## License

[CC BY 4.0](LICENSE): reuse freely, credit "Odile Labs, odilelabs.com/forwarding".
