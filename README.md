# j33pguy

Russ. Infrastructure and automation — Go, Nix, and the plumbing nobody demos.

Every repo here is a problem that started as a question I couldn't put down.
Most of them began with "wait, why is this manual?" and escalated. The one
that escalated furthest became [MAGI](https://github.com/j33pguy/magi).

Two operating rules. If I've done a thing by hand three times, I owe myself a
CLI for it. And I'd rather understand *why* something works than just get it
working today — small and weird this month beats big and polished never.

## Why does every AI session start from zero?

This one wouldn't let go. Switch machines: amnesia. Switch providers: context
gone. We're building on tools with no memory and pretending that's fine.

The residue:

**[magi](https://github.com/j33pguy/magi)** — Multi-Agent Graph Intelligence.
A universal memory server for AI agents. Self-hosted, model-agnostic,
Git-backed. Point every agent you run at one server and context survives
sessions, machines, and providers.

- Git-backed memory — every write is a commit; the database is a derived
  index, not the source of truth
- Hybrid retrieval — vector embeddings plus BM25
- Knowledge graph with behavioral pattern detection
- Speaks MCP, gRPC, REST, and ships a web UI

[getmagi.dev](https://getmagi.dev) · [Wiki](https://github.com/j33pguy/magi/wiki)

Which opened the next hole: memory that survives is memory that can drift.
**[magi-sync](https://github.com/j33pguy/magi-sync)** keeps it consistent
across machines.

## Do I actually own this?

I ask it of everything holding my stuff, and the answer keeps coming back no.
If the thing storing my notes, my infrastructure, or my family's calendar can
be discontinued by someone else's roadmap, I don't own it — I own a
subscription. So almost everything I run, I self-host. No telemetry, no
phoning home, no renting my own data back from someone.

## How did this box get like this?

Every host here has to answer that question from a repo and nothing else —
otherwise it's a liability, not a server. Golden images, declarative
infrastructure, config management, secrets in an actual secrets manager
instead of a `.env` file and a prayer. Those repos stay private, for the same
reason you don't publish a map of your house — but the philosophy is the
whole point. The day I can't answer is the day the box owns me instead.

## How deep does a shell config go?

Unclear; still digging. One repo per tool, so any single piece can be dropped
in on its own — wired together by home-manager across macOS, NixOS, and WSL.
And when one breaks, I get to find out exactly why.

| | |
|---|---|
| [zsh](https://github.com/j33pguy/zsh) | powerlevel10k, homebrew integration |
| [nvim](https://github.com/j33pguy/nvim) | lazy.nvim, go.nvim, telescope, neo-tree |
| [tmux](https://github.com/j33pguy/tmux) | tpm, vi mode, catppuccin-inspired |
| [fonts](https://github.com/j33pguy/fonts) | patched Nerd Fonts — MesloLGS NF Hitchhiker |

## Why is there game tooling in here?

Because I play games the way I run servers — eventually something gets
automated. A few repos here are companion tooling for games I play;
occupational hazard.

The handle? No Jeep in the driveway these days. It comes from my first one —
the thing that taught me to follow a trail just to see where it goes. The
vehicle went; the instinct didn't.

## Open questions

- **Rust.** Learning it the slow way, one small tool at a time.
- **The shelf.** Unfinished projects accumulating quietly. It's supposed to
  be for finishing, not collecting. I'm not always winning that one.

## Reach me

Profile-speak for all of the above is "passionately curious, loves solving
problems." True. The mechanism is less flattering: I am unable to leave a
thread alone.

russ@seaman.tech — best openers are "how does this work," "you're wrong about
this," and "nobody's solved this yet."
