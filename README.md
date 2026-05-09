# NotebookLM × Claude Code — твоя память без затрат

Лендинг про связку **Google NotebookLM + Claude Code skill** как бесплатной research-памяти для AI-агентов.

## Что внутри

Однофайловая статика (`index.html`) — никаких билдов, никаких зависимостей. Деплоится на Vercel мгновенно.

## Главные тезисы

1. **NotebookLM от Google — бесплатен.** 1M токенов контекста, 300 документов на ноутбук, ест видео/PDF/аудио.
2. **Skill снимает 2 ограничения:** locked data (нет API) + no compute (только текст).
3. **Не жжёт токены Claude.** Гигантская research-база живёт в NotebookLM, а не в контексте Claude.
4. **Не требует Pinecone/Supabase.** Для личной работы агента вектор-базы не нужны.
5. **10 минут установки.** git clone + один Google-логин в браузере.

## Источники

- Skill (open-source MIT): https://github.com/PleasePrompto/notebooklm-skill
- NotebookLM: https://notebooklm.google.com
- Видео-источник идеи: https://youtu.be/PkOlfB3RY5Q (Jack Roberts)

## Локальный просмотр

```bash
open index.html
# или
python3 -m http.server 8080
```

## Деплой

Скилл `ship-to-vercel` в Claude Code:

```
"залей этот лендинг на гит и на версель"
```

Ручной вариант:

```bash
gh repo create notebooklm-claude-memory --public --source=. --remote=origin
git add -A && git commit -m "init"
git push -u origin main
vercel deploy --prod --yes
```

## Лицензия

MIT.
