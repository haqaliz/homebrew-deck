# haqaliz/homebrew-deck

Homebrew tap for [**Deck**](https://github.com/haqaliz/deck) — a set of small,
native macOS desktop widgets delivered as one WidgetKit extension.

```bash
brew install --cask --no-quarantine haqaliz/deck/deck
```

`--no-quarantine` is required until Deck is notarized: it is signed with an
Apple Development certificate, which Gatekeeper rejects for downloaded apps.
The flag is what saves you from running `xattr -dr com.apple.quarantine` by
hand. It goes away the day notarization lands.

Then add the widgets: right-click the desktop → **Edit Widgets…** → **Deck**.

## Note for maintainers

`Casks/deck.rb` is a **mirror**. The source of truth is
[`homebrew/deck.rb`](https://github.com/haqaliz/deck/blob/master/homebrew/deck.rb)
in the Deck repo; edit it there, then copy it here. Every release bumps
`version` and pastes the DMG's `sha256` from that release's `SHA256SUMS.txt`.
