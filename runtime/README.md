# ASSEC LS Runtime — Migração paralela

Esta branch é isolada da publicação do formulário emergencial.

Objetivo: permitir migração sem interrupção perceptível ao associado.

Estado inicial:
- Vercel como gateway de compatibilidade;
- ASSEC legado continua como upstream enquanto cada módulo é convertido;
- cookies e redirecionamentos são reescritos para o novo host;
- respostas binárias (PDF, imagens e mídia) são transmitidas pelo gateway;
- quando o upstream não responde, o Runtime mostra fallback institucional e mantém acesso ao Vou Hoje emergencial;
- nenhum arquivo desta branch altera a branch `main` ou o GitHub Pages atual.

Base funcional analisada para a migração: ASSEC V29.53.

Importante: esta etapa não representa ainda a remoção integral do MySQL. Autenticação, financeiro, Mercado Pago, WebAuthn, Push, e-mail e demais dados compartilhados só podem ser retirados do backend legado quando houver armazenamento persistente seguro de arquivos/objetos para o Runtime.
