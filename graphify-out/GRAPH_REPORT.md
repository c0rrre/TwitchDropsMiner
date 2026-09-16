# Graph Report - TwitchDropsMiner  (2026-09-16)

## Corpus Check
- 50 files · ~54,559 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 824 nodes · 2232 edges · 47 communities (34 shown, 13 thin omitted)
- Extraction: 71% EXTRACTED · 29% INFERRED · 0% AMBIGUOUS · INFERRED: 658 edges (avg confidence: 0.52)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `7a293d40`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

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
- JsonType
- .check_online
- graphify reference: extra exports and benchmark
- .on_channel_update
- .get_spade_url
- GQLPersistedQuery
- graphify reference: query, path, explain
- graphify reference: add a URL and watch a folder
- graphify reference: commit hook and native CLAUDE.md integration
- graphify reference: incremental update and cluster-only
- graphify reference: GitHub clone and cross-repo merge
- graphify reference: transcribe video and audio
- CLAUDE.md
- CLAUDE.md
- extraction-spec.md

## God Nodes (most connected - your core abstractions)
1. `Twitch` - 136 edges
2. `Channel` - 107 edges
3. `MinerException` - 80 edges
4. `DropsCampaign` - 73 edges
5. `TimedDrop` - 67 edges
6. `Game` - 60 edges
7. `Settings` - 58 edges
8. `GUIManager` - 57 edges
9. `ExitRequest` - 47 edges
10. `PriorityMode` - 46 edges

## Surprising Connections (you probably didn't know these)
- `CAPTCHA (fatal exit condition)` --semantically_similar_to--> `Same-account dual-watch warning`  [INFERRED] [semantically similar]
  manual.txt → README.md
- `ExpiringHash` --uses--> `GUIManager`  [INFERRED]
  cache.py → gui.py
- `ImageCache` --uses--> `GUIManager`  [INFERRED]
  cache.py → gui.py
- `CampaignProgress` --uses--> `ImageCache`  [INFERRED]
  gui.py → cache.py
- `ChannelList` --uses--> `ImageCache`  [INFERRED]
  gui.py → cache.py

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **graphify SKILL.md and its reference documents** — _claude_skills_graphify_skill_document, _claude_skills_graphify_references_add_watch_document, _claude_skills_graphify_references_exports_document, _claude_skills_graphify_references_extraction_spec_document, _claude_skills_graphify_references_github_and_merge_document, _claude_skills_graphify_references_hooks_document, _claude_skills_graphify_references_query_document, _claude_skills_graphify_references_transcribe_document, _claude_skills_graphify_references_update_document [EXTRACTED 1.00]
- **GitHub repository automation configs** — _github_funding_document, _github_dependabot_document, _github_pull_document, _github_workflows_check_patch_notes_document [INFERRED 0.85]
- **Twitch API interaction (GQL, websocket, HTTP)** — patch_notes_gql_persisted_queries, readme_sharded_websocket, requirements_aiohttp [INFERRED 0.75]

## Communities (47 total, 13 thin omitted)

### Community 0 - "GUI Core & Campaign Display"
Cohesion: 0.06
Nodes (65): ImageCache, PriorityMode, Enum, State, ExitRequest, Raised when the application is requested to exit from outside of the main loop., Flag, _GridInfo (+57 more)

### Community 1 - "Channel Model"
Cohesion: 0.10
Nodes (8): Channel, Returns a string to be used as ID/key of the columns inside channel list., Returns True if the streamer is online and is currently streaming, False otherwi, Returns True if the streamer is offline and isn't about to come online, False ot, Returns True if the streamer is about to go online (most likely), False otherwis, # NOTE: This is currently unused., # NOTE: the CDN is configured to forcibly disconnect shortly after serving the l, # NOTE: This is currently unused.

### Community 2 - "WebSocket Topics & Client"
Cohesion: 0.06
Nodes (12): ClientWebSocketResponse, WebsocketTopic, Raised when the websocket connection has been closed.      Attributes:     -----, WebsocketClosed, TopicProcess, ExponentialBackoff, Any, JsonType (+4 more)

### Community 3 - "Drop Inventory Logic"
Cohesion: 0.06
Nodes (18): BaseDrop, Benefit, BenefitType, datetime, Enum, JsonType, URLType, # NOTE: This does not check the campaign's eligibility or active status (+10 more)

### Community 4 - "GUI Channel List"
Cohesion: 0.07
Nodes (9): _Anchor, CampaignProgress, ChannelList, main(), main_exit(), Requests the GUI application to close.         The window itself will be closed, Closes the window. Invalidates the logger., TrayIcon (+1 more)

### Community 5 - "Project Docs & Patch Notes"
Cohesion: 0.05
Nodes (43): .github/dependabot.yml, .github/FUNDING.yml, .github/pull.yml (upstream auto-merge), check_patch_notes.yml workflow, CAPTCHA (fatal exit condition), manual.txt (CLI usage), patch_notes.txt (changelog), GQL persisted queries (Twitch API) (+35 more)

### Community 6 - "Exceptions & Translations"
Cohesion: 0.13
Nodes (30): MinerException, Exception, Base exception class for this application., ChromeMessages, ErrorMessages, GUIChannelHeadings, GUIChannels, GUIHelp (+22 more)

### Community 7 - "Exception Types"
Cohesion: 0.14
Nodes (13): CaptchaRequired, GQLException, LoginException, Raised when the application is requested to reload entirely, without closing the, Raised for cases where a web request doesn't return what we wanted it to., Raised when a request becomes no longer valid inside its retry loop.      Intend, Raised when an exception occurs during login phase., The most dreaded thing about automated scripts... (+5 more)

### Community 8 - "GUI Manager Core"
Cohesion: 0.14
Nodes (6): GUIManager, This function serves as a message processor for all messages sent         to the, This runs the Tkinter event loop via asyncio instead of calling mainloop., Label, StringVar, Widget

### Community 9 - "GUI Settings Panel"
Cohesion: 0.15
Nodes (4): Combobox, Path, If we're empty, insert a placeholder, set placeholder text color and make sure i, SettingsPanel

### Community 10 - "Twitch Client Rationale"
Cohesion: 0.09
Nodes (20): Any, # NOTE: In these cases, channel was the watching channel, # NOTE: In these cases, it wasn't the watching channel, # NOTE: this fetches pictures from the CDN, so might be slow without a cache, # NOTE: maintenance task is restarted at the end of each inventory fetch, # NOTE: Have to do this here, becase "channels" can be any iterable, # NOTE: GQL is pretty volatile and breaks everything if one runs into their rate, # NOTE: Unfortunately, aiohttp provides no easy way of clearing empty cookies, (+12 more)

### Community 11 - "GUI Theming Widgets"
Cohesion: 0.13
Nodes (5): Any, Tk, Set the Windows title bar color to match the theme.         Only works on Window, Apply dark/light palette to ttk styles and Tk widgets in a minimal, non-invasive, TK_PADDING

### Community 12 - "CLI Entry & Argument Parsing"
Cohesion: 0.12
Nodes (13): main(), Parser, NoReturn, # NOTE: we have to do it after wait_until_closed,, # TODO: replace int with union of literal values once typeshed updates, # NOTE: parser output is shown via message box, PhotoImage, SupportsWrite (+5 more)

### Community 13 - "Async Utilities"
Cohesion: 0.08
Nodes (24): For /graphify add and --watch, For /graphify query, For the commit hook and native CLAUDE.md integration, For --update and --cluster-only, /graphify, Honesty Rules, Interpreter guard for subcommands, Part A - Structural extraction for code files (+16 more)

### Community 14 - "Image Cache"
Cohesion: 0.12
Nodes (10): ExpiringHash, datetime, TypedDict, URLType, # NOTE: If self._hashes ever stops being updated in both above if cases,, # NOTE: The hashes are deleted from self._hashes above, Image, ImageHash (+2 more)

### Community 15 - "GUI Overlay Widgets"
Cohesion: 0.13
Nodes (5): Event, _T, If we've had a placeholder, clear the box and set normal text colour and show., Misc, _Relief

### Community 16 - "Twitch Drops Processing"
Cohesion: 0.20
Nodes (4): GQLOperation, JsonType, Utilize batch GQL requests to check ONLINE status for a lot of channels at once., chunk()

### Community 17 - "GQL Constants"
Cohesion: 0.22
Nodes (8): ClientType, Path, # NOTE: These don't have to be available to the end-user, so the path points to, Get an absolute path to a bundled resource.      Works for dev and for PyInstall, # NOTE: This modifies base in place, # NOTE: pyinstaller will set sys.argv[0] to its own executable when building, # NOTE: sys.argv[0] will point to gui.py when running the gui.py directly for GU, _resource_path()

### Community 18 - "Twitch Watch Loop"
Cohesion: 0.26
Nodes (4): NoReturn, Called when the application is requested to close by the user,         usually b, Saves the application state., Main method that runs the whole client.          Here, we manage several things,

### Community 19 - "Twitch Auth Session"
Cohesion: 0.20
Nodes (5): ClientResponse, ClientSession, _AuthState, datetime, URL

### Community 20 - "GUI Placeholder Entry Widget"
Cohesion: 0.20
Nodes (6): Stream, GQLQuery, SupportsInt, isonow(), json_minify(), Returns minified JSON for payload usage.

### Community 21 - "Graphify Skill Docs"
Cohesion: 0.26
Nodes (12): graphify reference: add-watch.md, graphify reference: exports.md, graphify reference: extraction-spec.md, graphify reference: github-and-merge.md, graphify reference: hooks.md, graphify reference: query.md, graphify reference: transcribe.md, graphify reference: update.md (+4 more)

### Community 23 - "Async Value & Link Widget"
Cohesion: 0.11
Nodes (14): BaseException, _D, _P, AwaitableValue, deduplicate(), first_to_complete(), format_traceback(), Any (+6 more)

### Community 26 - "CLI Args & Settings"
Cohesion: 0.25
Nodes (4): ParsedArgs, If the debug flag is True, return DEBUG.             If the main logging level i, TypedDict, SettingsFile

### Community 27 - "JSON Utils"
Cohesion: 0.22
Nodes (11): _JSON_T, create_nonce(), _deserialize(), json_load(), merge_json(), JsonType, # NOTE: IntEnum cannot be used, as it will get serialized as a plain integer,, # NOTE: This modifies object in place (+3 more)

### Community 33 - ".check_online"
Cohesion: 0.22
Nodes (4): Fetches the current channel stream, and if one exists,         updates it's game, The 'stream-up' event is sent before the stream actually goes online,         so, Sets up a task that will wait ONLINE_DELAY duration,         and then check for, Sets the channel status to OFFLINE. Cancels PENDING_ONLINE if applicable.

### Community 34 - "graphify reference: extra exports and benchmark"
Cohesion: 0.22
Nodes (8): graphify reference: extra exports and benchmark, Step 6b - Wiki (only if --wiki flag), Step 7 - Neo4j export (only if --neo4j or --neo4j-push flag), Step 7a - FalkorDB export (only if --falkordb or --falkordb-push flag), Step 7b - SVG export (only if --svg flag), Step 7c - GraphML export (only if --graphml flag), Step 7d - MCP server (only if --mcp flag), Step 8 - Token reduction benchmark (only if total_words > 5000)

### Community 35 - ".on_channel_update"
Cohesion: 0.25
Nodes (4): Determines if the given channel qualifies as a switch candidate., Called by a Channel when it's status is updated (ONLINE, OFFLINE, title/tags cha, Return a priority number for a given channel.          0 has the highest priorit, Determines if the given channel qualifies as a watching candidate.

### Community 36 - ".get_spade_url"
Cohesion: 0.29
Nodes (3): URLType, To get this monstrous thing, you have to walk a chain of requests.         Strea, This performs a HEAD request on the stream's current playlist,         to simula

### Community 37 - "GQLPersistedQuery"
Cohesion: 0.43
Nodes (3): GQLPersistedQuery, _merge_vars(), JsonType

### Community 38 - "graphify reference: query, path, explain"
Cohesion: 0.33
Nodes (5): For /graphify explain, For /graphify path, graphify reference: query, path, explain, Step 0 — Constrained query expansion (REQUIRED before traversal), Step 1 — Traversal

### Community 39 - "graphify reference: add a URL and watch a folder"
Cohesion: 0.50
Nodes (3): For /graphify add, For --watch, graphify reference: add a URL and watch a folder

### Community 40 - "graphify reference: commit hook and native CLAUDE.md integration"
Cohesion: 0.50
Nodes (3): For git commit hook, For native CLAUDE.md integration, graphify reference: commit hook and native CLAUDE.md integration

### Community 41 - "graphify reference: incremental update and cluster-only"
Cohesion: 0.50
Nodes (3): For --cluster-only, For --update (incremental re-extraction), graphify reference: incremental update and cluster-only

## Knowledge Gaps
- **76 isolated node(s):** `build.sh script`, `setup_env.sh script`, `graphify`, `Usage`, `What graphify is for` (+71 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **13 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Twitch` connect `Twitch Client Rationale` to `GUI Core & Campaign Display`, `Channel Model`, `WebSocket Topics & Client`, `Drop Inventory Logic`, `GUI Channel List`, `Exceptions & Translations`, `Exception Types`, `GUI Manager Core`, `GUI Settings Panel`, `GUI Theming Widgets`, `CLI Entry & Argument Parsing`, `Twitch Drops Processing`, `GQL Constants`, `Twitch Watch Loop`, `Twitch Auth Session`, `GUI Placeholder Entry Widget`, `GUI Inventory Overview`, `Async Value & Link Widget`, `Rate Limiter`, `CLI Args & Settings`, `JSON Utils`, `Client Info Constants`, `JsonType`, `.on_channel_update`?**
  _High betweenness centrality (0.210) - this node is a cross-community bridge._
- **Why does `Channel` connect `Channel Model` to `GUI Core & Campaign Display`, `Drop Inventory Logic`, `GUI Channel List`, `Exceptions & Translations`, `Exception Types`, `GUI Manager Core`, `GUI Settings Panel`, `Twitch Client Rationale`, `Twitch Drops Processing`, `GQL Constants`, `Twitch Watch Loop`, `Twitch Auth Session`, `GUI Placeholder Entry Widget`, `GUI Inventory Overview`, `JSON Utils`, `JsonType`, `.check_online`, `.on_channel_update`, `.get_spade_url`, `GQLPersistedQuery`?**
  _High betweenness centrality (0.127) - this node is a cross-community bridge._
- **Why does `MinerException` connect `Exceptions & Translations` to `JsonType`, `Channel Model`, `GUI Core & Campaign Display`, `WebSocket Topics & Client`, `.get_spade_url`, `GUI Channel List`, `Exception Types`, `GUI Manager Core`, `GUI Settings Panel`, `Twitch Client Rationale`, `Twitch Drops Processing`, `Twitch Auth Session`, `GUI Placeholder Entry Widget`, `GUI Inventory Overview`?**
  _High betweenness centrality (0.073) - this node is a cross-community bridge._
- **Are the 60 inferred relationships involving `Twitch` (e.g. with `Channel` and `Stream`) actually correct?**
  _`Twitch` has 60 INFERRED edges - model-reasoned connections that need verification._
- **Are the 44 inferred relationships involving `Channel` (e.g. with `GQLPersistedQuery` and `GQLQuery`) actually correct?**
  _`Channel` has 44 INFERRED edges - model-reasoned connections that need verification._
- **Are the 67 inferred relationships involving `MinerException` (e.g. with `Channel` and `.get_spade_url()`) actually correct?**
  _`MinerException` has 67 INFERRED edges - model-reasoned connections that need verification._
- **Are the 39 inferred relationships involving `DropsCampaign` (e.g. with `_BaseVars` and `_Buttons`) actually correct?**
  _`DropsCampaign` has 39 INFERRED edges - model-reasoned connections that need verification._