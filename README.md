# hangel for Claude

Find volunteering opportunities, plan NGO events and volunteer calls, scan open grant and funding calls, and shop for donations on [hangel](https://hangel.org), a Turkiye-based social impact platform. The plugin bundles four skills and connects Claude to hangel's public, read-only connector. [Türkçe bölüm aşağıda.](#türkçe)

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

**Veri ve gizlilik.** Eklenti bilgisayarınızda hiçbir şey çalıştırmaz ve hiçbir şey saklamaz. Bir beceri bağlayıcıyı kullandığında Claude, `https://hangel.org/api/mcp` adresine yalnızca arama ifadesini ve süzgeçleri (sözcük, şehir, sonuç sayısı) gönderir; bağlayıcı hangel.org’da zaten herkese açık olan kayıtları döndürür. Hesap, ad ya da e-posta istenmez; sohbetiniz okunmaz. Gizli, yalnız davetlilere ya da çalışanlara özel, test ve gösterim kayıtları dışarıda tutulur. Gizlilik politikası: <https://hangel.org/policies/privacy>.

**Sınırlar.** Kayıtların çoğu Türkçedir. Bağlayıcı salt okurdur: başvuru yapmaz, kayıt oluşturmaz, etkinlik açmaz, satın alma yapmaz. Bu eklentiyi hangel geliştirir ve işletir; Anthropic ürünü değildir. Destek: info@hangel.org.
