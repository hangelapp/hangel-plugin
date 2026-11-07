# hangel for Claude

Find volunteering opportunities, plan NGO events and volunteer calls, scan open grant and funding calls, and shop for donations on [hangel](https://hangel.org), a Turkiye-based social impact platform. The plugin bundles four skills and connects Claude to hangel's public, read-only connector. It also installs as a [Gemini CLI extension](#install-in-gemini-cli) and an Antigravity CLI plugin. [Türkçe bölüm aşağıda.](#türkçe)

## What is in the plugin

| Skill | Use it when |
| --- | --- |
| `find-volunteering` | You want to find where to volunteer by city, cause, skills or online. |
| `plan-ngo-event-call` | An NGO, club or institution plans an event and needs a volunteer call and announcement. |
| `scan-funding-calls` | You want to shortlist the grant and funding calls that are open now. |
| `shop-and-donate` | You want to understand hangel Market donation rates and compare products or stores. |

The plugin's `.mcp.json` points at `https://hangel.org/api/mcp` (Streamable HTTP, no authentication). The connector exposes ten read-only tools: `search`, `fetch`, `search_ngos`, `list_events`, `list_volunteering`, `list_open_funds`, `search_products`, `list_stores`, `search_library` and `platform_info`. Full documentation, example prompts and the server card are at <https://hangel.org/developers/claude>.

## Install

- **claude.ai or Claude Desktop:** zip this folder, then open Customize > Plugins > Add > Upload plugin and select the zip. Connect the bundled connector from the plugin's Connectors tab.
- **Claude Code:** run `claude --plugin-dir ./hangel-plugin` from the folder that contains this one, or install it from a marketplace once it is listed.

## Install in Gemini CLI

The same repository is also a [Gemini CLI extension](https://geminicli.com/docs/extensions/) (`gemini-extension.json` and `GEMINI.md` at the root). It connects Gemini CLI to the same public MCP server (`httpUrl`: `https://hangel.org/api/mcp`) and loads the four skills above.

```sh
gemini extensions install https://github.com/hangelapp/hangel-plugin
```

Restart Gemini CLI, then check with `gemini extensions list` and `gemini mcp list`. Update later with `gemini extensions update hangel`.

Since 18 June 2026 Google serves Gemini CLI to Gemini Code Assist Standard and Enterprise licences and to paid API keys; Google AI Pro, Ultra and free-tier accounts use Antigravity CLI instead. For Antigravity CLI the repository also carries a `plugin.json` and an `mcp_config.json` at the root:

```sh
agy plugin install https://github.com/hangelapp/hangel-plugin
```

This is not a Google product. Gemini and Antigravity are trademarks of Google.

## Example prompts

- "What environmental volunteering opportunities are open right now?"
- "Help our NGO plan a tree-planting day in November and write the volunteer call."
- "Which grant and funding calls for youth organisations are open now? Sort them by deadline."
- "Show running shoes on hangel Market, starting with the highest donation rate."

## Data and privacy

The plugin runs nothing on your computer and stores nothing. When a skill uses the connector, Claude sends only the search phrase and filters (such as a keyword, a city or a limit) to `https://hangel.org/api/mcp`, and the connector returns records that are already public on hangel.org. No account, name or email is requested, and your conversation is not read. Private, invite-only, employee-only, test and demo records are excluded. Standard server logs at hangel can include technical request data such as IP address and time. Privacy policy: <https://hangel.org/policies/privacy>.

## Limits

Most records are in Turkish. The connector is read-only: it cannot apply, register, create events or buy. Fair use is 120 requests per minute per IP address. hangel builds and runs this plugin. It is not an Anthropic product, and Claude is a trademark of Anthropic.

## Support

Questions, bug reports and security matters: info@hangel.org. Help center: <https://hangel.org/support>. To report a vulnerability, see <https://hangel.org/guvenlik#acik-bildirimi>.

## License

MIT, see [LICENSE](LICENSE).

---

## Türkçe

hangel’ın herkese açık, salt okur bağlayıcısını Claude’a bağlar ve dört beceri ekler: gönüllülük fırsatı bulma (`find-volunteering`), STK için etkinlik ve gönüllü çağrısı planlama (`plan-ngo-event-call`), açık hibe ve fon çağrılarını tarama (`scan-funding-calls`) ve hangel Market’te alışverişten bağış oranlarını anlama ve karşılaştırma (`shop-and-donate`).

**Kurulum.** claude.ai ya da Claude masaüstü: klasörü zipleyin, Özelleştir > Eklentiler > Ekle > Eklenti yükle yolundan yükleyin; ardından eklentinin Bağlayıcılar sekmesinden hangel bağlayıcısını bağlayın. Claude Code: `claude --plugin-dir ./hangel-plugin`.

**Gemini CLI’ye kurulum.** Aynı depo bir Gemini CLI uzantısıdır (kökte `gemini-extension.json` ve `GEMINI.md`): aynı herkese açık MCP sunucusuna bağlar ve dört beceriyi yükler. Kurmak için `gemini extensions install https://github.com/hangelapp/hangel-plugin` komutunu çalıştırın, Gemini CLI’yi yeniden başlatın ve `gemini extensions list` ile `gemini mcp list` ile denetleyin. Google, 18 Haziran 2026’dan beri Gemini CLI’yi Gemini Code Assist Standard ve Enterprise lisanslarına ve ücretli API anahtarlarına sunuyor; Google AI Pro, Ultra ve ücretsiz bireysel hesaplar Antigravity CLI kullanıyor. Antigravity CLI için depoda kökte `plugin.json` ve `mcp_config.json` da var: `agy plugin install https://github.com/hangelapp/hangel-plugin`. Bu bir Google ürünü değildir; Gemini ve Antigravity Google’ın markalarıdır.

**Veri ve gizlilik.** Eklenti bilgisayarınızda hiçbir şey çalıştırmaz ve hiçbir şey saklamaz. Bir beceri bağlayıcıyı kullandığında Claude, `https://hangel.org/api/mcp` adresine yalnızca arama ifadesini ve süzgeçleri (sözcük, şehir, sonuç sayısı) gönderir; bağlayıcı hangel.org’da zaten herkese açık olan kayıtları döndürür. Hesap, ad ya da e-posta istenmez; sohbetiniz okunmaz. Gizli, yalnız davetlilere ya da çalışanlara özel, test ve gösterim kayıtları dışarıda tutulur. Gizlilik politikası: <https://hangel.org/policies/privacy>.

**Sınırlar.** Kayıtların çoğu Türkçedir. Bağlayıcı salt okurdur: başvuru yapmaz, kayıt oluşturmaz, etkinlik açmaz, satın alma yapmaz. Bu eklentiyi hangel geliştirir ve işletir; Anthropic ürünü değildir. Destek: info@hangel.org.
