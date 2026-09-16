# Graph Report - .  (2026-09-16)

## Corpus Check
- 57 files · ~51,783 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 736 nodes · 2142 edges · 32 communities (25 shown, 7 thin omitted)
- Extraction: 69% EXTRACTED · 31% INFERRED · 0% AMBIGUOUS · INFERRED: 654 edges (avg confidence: 0.52)
- Token cost: 165,232 input · 0 output

## Community Hubs (Navigation)
- GUI Core & Campaign Display
- Channel Model
- WebSocket Topics & Client
- Drop Inventory Logic
- GUI Channel List
- Project Docs & Patch Notes
- Exceptions & Translations
- Exception Types
- GUI Manager Core
- GUI Settings Panel
- Twitch Client Rationale
- GUI Theming Widgets
- CLI Entry & Argument Parsing
- Async Utilities
- Image Cache
- GUI Overlay Widgets
- Twitch Drops Processing
- GQL Constants
- Twitch Watch Loop
- Twitch Auth Session
- GUI Placeholder Entry Widget
- Graphify Skill Docs
- GUI Inventory Overview
- Async Value & Link Widget
- GUI Login Flow
- Rate Limiter
- CLI Args & Settings
- JSON Utils
- Client Info Constants
- Build Script
- Setup Script
- AppImage Icon

## God Nodes (most connected - your core abstractions)
1. `Twitch` - 137 edges
2. `Channel` - 102 edges
3. `MinerException` - 78 edges
4. `DropsCampaign` - 73 edges
5. `TimedDrop` - 67 edges
6. `Game` - 59 edges
7. `Settings` - 58 edges
8. `GUIManager` - 56 edges
9. `ExitRequest` - 47 edges
10. `PriorityMode` - 46 edges

## Surprising Connections (you probably didn't know these)
- `CAPTCHA (fatal exit condition)` --semantically_similar_to--> `Same-account dual-watch warning`  [INFERRED] [semantically similar]
  manual.txt → README.md
- `ExpiringHash` --uses--> `GUIManager`  [INFERRED]
  cache.py → gui.py
- `ImageCache` --uses--> `GUIManager`  [INFERRED]
  cache.py → gui.py
- `ChannelList` --uses--> `ImageCache`  [INFERRED]
  gui.py → cache.py
- `InventoryOverview` --uses--> `ImageCache`  [INFERRED]
  gui.py → cache.py

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **graphify SKILL.md and its reference documents** — _claude_skills_graphify_skill_document, _claude_skills_graphify_references_add_watch_document, _claude_skills_graphify_references_exports_document, _claude_skills_graphify_references_extraction_spec_document, _claude_skills_graphify_references_github_and_merge_document, _claude_skills_graphify_references_hooks_document, _claude_skills_graphify_references_query_document, _claude_skills_graphify_references_transcribe_document, _claude_skills_graphify_references_update_document [EXTRACTED 1.00]
- **GitHub repository automation configs** — _github_funding_document, _github_dependabot_document, _github_pull_document, _github_workflows_check_patch_notes_document [INFERRED 0.85]
- **Twitch API interaction (GQL, websocket, HTTP)** — patch_notes_gql_persisted_queries, readme_sharded_websocket, requirements_aiohttp [INFERRED 0.75]

## Communities (32 total, 7 thin omitted)

### Community 0 - "GUI Core & Campaign Display"
Cohesion: 0.06
Nodes (60): ImageCache, PriorityMode, Enum, State, ExitRequest, Raised when the application is requested to exit from outside of the main loop., Flag, _GridInfo (+52 more)

### Community 1 - "Channel Model"
Cohesion: 0.05
Nodes (24): Channel, JsonType, URLType, Returns a string to be used as ID/key of the columns inside channel list., Returns True if the streamer is online and is currently streaming, False otherwi, Returns True if the streamer is offline and isn't about to come online, False ot, Returns True if the streamer is about to go online (most likely), False otherwis, To get this monstrous thing, you have to walk a chain of requests.         Strea (+16 more)

### Community 2 - "WebSocket Topics & Client"
Cohesion: 0.06
Nodes (12): ClientWebSocketResponse, WebsocketTopic, _P, TopicProcess, ExponentialBackoff, task_wrapper(), Any, JsonType (+4 more)

### Community 3 - "Drop Inventory Logic"
Cohesion: 0.06
Nodes (16): BaseDrop, Benefit, BenefitType, datetime, Enum, JsonType, URLType, # NOTE: This does not check the campaign's eligibility or active status (+8 more)

### Community 4 - "GUI Channel List"
Cohesion: 0.07
Nodes (12): _Anchor, ChannelList, create_channel(), create_drop(), create_game(), main(), main_exit(), Requests the GUI application to close.         The window itself will be closed (+4 more)

### Community 5 - "Project Docs & Patch Notes"
Cohesion: 0.07
Nodes (32): .github/dependabot.yml, .github/FUNDING.yml, .github/pull.yml (upstream auto-merge), check_patch_notes.yml workflow, CAPTCHA (fatal exit condition), manual.txt (CLI usage), patch_notes.txt (changelog), GQL persisted queries (Twitch API) (+24 more)

### Community 6 - "Exceptions & Translations"
Cohesion: 0.14
Nodes (28): MinerException, Exception, Base exception class for this application., ChromeMessages, ErrorMessages, GUIChannelHeadings, GUIChannels, GUIHelp (+20 more)

### Community 7 - "Exception Types"
Cohesion: 0.12
Nodes (15): CaptchaRequired, GQLException, LoginException, Raised when the application is requested to reload entirely, without closing the, Raised for cases where a web request doesn't return what we wanted it to., Raised when a request becomes no longer valid inside its retry loop.      Intend, Raised when the websocket connection has been closed.      Attributes:     -----, Raised when an exception occurs during login phase. (+7 more)

### Community 8 - "GUI Manager Core"
Cohesion: 0.16
Nodes (6): GUIManager, This function serves as a message processor for all messages sent         to the, This runs the Tkinter event loop via asyncio instead of calling mainloop., Label, StringVar, Widget

### Community 9 - "GUI Settings Panel"
Cohesion: 0.16
Nodes (3): Combobox, Path, SettingsPanel

### Community 10 - "Twitch Client Rationale"
Cohesion: 0.09
Nodes (20): Any, # NOTE: In these cases, channel was the watching channel, # NOTE: In these cases, it wasn't the watching channel, # NOTE: this fetches pictures from the CDN, so might be slow without a cache, # NOTE: maintenance task is restarted at the end of each inventory fetch, # NOTE: Have to do this here, becase "channels" can be any iterable, # NOTE: GQL is pretty volatile and breaks everything if one runs into their rate, # NOTE: Unfortunately, aiohttp provides no easy way of clearing empty cookies, (+12 more)

### Community 11 - "GUI Theming Widgets"
Cohesion: 0.14
Nodes (5): Any, Tk, Apply dark/light palette to ttk styles and Tk widgets in a minimal, non-invasive, set_theme(), TK_PADDING

### Community 12 - "CLI Entry & Argument Parsing"
Cohesion: 0.12
Nodes (13): main(), Parser, NoReturn, # NOTE: we have to do it after wait_until_closed,, # TODO: replace int with union of literal values once typeshed updates, # NOTE: parser output is shown via message box, PhotoImage, SupportsWrite (+5 more)

### Community 13 - "Async Utilities"
Cohesion: 0.18
Nodes (14): BaseException, deduplicate(), first_to_complete(), format_traceback(), Any, datetime, _T, # NOTE: IntEnum cannot be used, as it will get serialized as a plain integer, (+6 more)

### Community 14 - "Image Cache"
Cohesion: 0.12
Nodes (10): ExpiringHash, datetime, TypedDict, URLType, # NOTE: If self._hashes ever stops being updated in both above if cases,, # NOTE: The hashes are deleted from self._hashes above, Image, ImageHash (+2 more)

### Community 15 - "GUI Overlay Widgets"
Cohesion: 0.16
Nodes (3): Event, Misc, _Relief

### Community 16 - "Twitch Drops Processing"
Cohesion: 0.22
Nodes (3): JsonType, Utilize batch GQL requests to check ONLINE status for a lot of channels at once., chunk()

### Community 17 - "GQL Constants"
Cohesion: 0.17
Nodes (11): ClientType, GQLOperation, _merge_vars(), JsonType, Path, # NOTE: These don't have to be available to the end-user, so the path points to, Get an absolute path to a bundled resource.      Works for dev and for PyInstall, # NOTE: This modifies base in place (+3 more)

### Community 18 - "Twitch Watch Loop"
Cohesion: 0.21
Nodes (4): NoReturn, Called when the application is requested to close by the user,         usually b, Saves the application state., Main method that runs the whole client.          Here, we manage several things,

### Community 19 - "Twitch Auth Session"
Cohesion: 0.20
Nodes (6): ClientResponse, ClientSession, _AuthState, datetime, URL, create_nonce()

### Community 20 - "GUI Placeholder Entry Widget"
Cohesion: 0.27
Nodes (4): PlaceholderEntry, proxy_validate(), If we're empty, insert a placeholder, set placeholder text color and make sure i, If we've had a placeholder, clear the box and set normal text colour and show.

### Community 21 - "Graphify Skill Docs"
Cohesion: 0.26
Nodes (12): graphify reference: add-watch.md, graphify reference: exports.md, graphify reference: extraction-spec.md, graphify reference: github-and-merge.md, graphify reference: hooks.md, graphify reference: query.md, graphify reference: transcribe.md, graphify reference: update.md (+4 more)

### Community 23 - "Async Value & Link Widget"
Cohesion: 0.18
Nodes (4): _D, AwaitableValue, URL, webopen()

### Community 26 - "CLI Args & Settings"
Cohesion: 0.25
Nodes (4): ParsedArgs, If the debug flag is True, return DEBUG.             If the main logging level i, TypedDict, SettingsFile

### Community 27 - "JSON Utils"
Cohesion: 0.38
Nodes (6): _JSON_T, _deserialize(), json_load(), merge_json(), JsonType, _remove_missing()

## Knowledge Gaps
- **22 isolated node(s):** `build.sh script`, `setup_env.sh script`, `graphify reference: extraction-spec.md`, `graphify reference: github-and-merge.md`, `graphify reference: transcribe.md` (+17 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **7 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Twitch` connect `Twitch Client Rationale` to `GUI Core & Campaign Display`, `Channel Model`, `WebSocket Topics & Client`, `Drop Inventory Logic`, `GUI Channel List`, `Exceptions & Translations`, `Exception Types`, `GUI Manager Core`, `GUI Settings Panel`, `GUI Theming Widgets`, `CLI Entry & Argument Parsing`, `Async Utilities`, `Twitch Drops Processing`, `GQL Constants`, `Twitch Watch Loop`, `Twitch Auth Session`, `GUI Placeholder Entry Widget`, `GUI Inventory Overview`, `Async Value & Link Widget`, `Rate Limiter`, `CLI Args & Settings`, `Client Info Constants`?**
  _High betweenness centrality (0.263) - this node is a cross-community bridge._
- **Why does `Channel` connect `Channel Model` to `GUI Core & Campaign Display`, `Drop Inventory Logic`, `GUI Channel List`, `Exceptions & Translations`, `Exception Types`, `GUI Manager Core`, `GUI Settings Panel`, `Twitch Client Rationale`, `Async Utilities`, `Twitch Drops Processing`, `GQL Constants`, `Twitch Watch Loop`, `Twitch Auth Session`, `GUI Placeholder Entry Widget`, `GUI Inventory Overview`?**
  _High betweenness centrality (0.140) - this node is a cross-community bridge._
- **Why does `MinerException` connect `Exceptions & Translations` to `GUI Core & Campaign Display`, `Channel Model`, `WebSocket Topics & Client`, `GUI Channel List`, `Exception Types`, `GUI Manager Core`, `GUI Settings Panel`, `Twitch Client Rationale`, `Twitch Drops Processing`, `Twitch Watch Loop`, `Twitch Auth Session`, `GUI Placeholder Entry Widget`, `GUI Inventory Overview`?**
  _High betweenness centrality (0.086) - this node is a cross-community bridge._
- **Are the 61 inferred relationships involving `Twitch` (e.g. with `Channel` and `Stream`) actually correct?**
  _`Twitch` has 61 INFERRED edges - model-reasoned connections that need verification._
- **Are the 43 inferred relationships involving `Channel` (e.g. with `GQLOperation` and `MinerException`) actually correct?**
  _`Channel` has 43 INFERRED edges - model-reasoned connections that need verification._
- **Are the 65 inferred relationships involving `MinerException` (e.g. with `Channel` and `.get_spade_url()`) actually correct?**
  _`MinerException` has 65 INFERRED edges - model-reasoned connections that need verification._
- **Are the 39 inferred relationships involving `DropsCampaign` (e.g. with `_BaseVars` and `_Buttons`) actually correct?**
  _`DropsCampaign` has 39 INFERRED edges - model-reasoned connections that need verification._