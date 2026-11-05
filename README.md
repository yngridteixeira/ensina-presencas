# Ensina Brasil — Presenças

Demonstração privada no Sites e aplicação operacional para Render Web Service Free + Supabase Free, sem Background Worker pago. A demonstração não é o servidor real.

Abra **COMECE_AQUI.html** no computador para o roteiro visual. Evento: 11 a 16/01/2027, uma presença por participante + data + manhã/tarde. Os 12 períodos vêm com horários de exemplo e desativados.

Guia técnico: [docs/GUIA.md](docs/GUIA.md). Leia [docs/VALIDACAO.md](docs/VALIDACAO.md) para saber o que foi efetivamente testado e [docs/PILOTO.md](docs/PILOTO.md) para validar em celulares.

## Comandos

```sh
npm ci
npm run migrate
npm run bootstrap
npm run setup-event
npm start
```

Defina `SHEETS_SYNC_MODE=inline` e `SYNC_INTERVAL_MS=60000`: a sincronização roda no próprio site. Não crie Background Worker pago. Consulte **docs/CUSTO_ZERO.md** para planos e limites gratuitos.

Testes: `npm test`. Teste de oito conexões reais requer `TEST_DATABASE_URL` de homologação.

Não publique `.env`, chaves ou backups. Configure as variáveis a partir de `.env.example`. Código da interface em `dist`, API em `server`, esquema em `db`, exemplos em `examples`.
