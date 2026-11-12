# 📊 Painel de Coordenação Pro

Painel web de gestão para a coordenação do **Abrigo Bom Jesus (ADRA)**. Reúne em uma única tela o controle de funcionários, atas, acolhidos, patrimônio e fluxo financeiro, com visual escuro e layout responsivo (celular e computador).

> Aplicação em **HTML único**, sem etapa de build, com banco de dados na nuvem via **Supabase**.

## ✨ Funcionalidades

- **👥 Funcionários** – cadastro com foto, função, horário, equipe, checklist de documentos (docs, ASO, contrato, uniforme, EPI), alinhamentos e advertências; importação em lote por planilha Excel.
- **📝 Atas** – registro e consulta de atas de reunião.
- **📅 Agenda de eventos** – calendário responsivo para agendar eventos.
- **🏠 Acolhidos** – visão geral de acolhidos e camas livres, com prontuário e histórico de registros.
- **🗂️ D.P. (Departamento Pessoal)** – módulo de apoio à documentação de pessoal.
- **🏷️ Patrimônio** – controle de bens, com upload de arquivos.
- **💰 Financeiro** – fluxo digital de notas fiscais: leitura de **QR Code** (extrai valor e chave de acesso de 44 dígitos) com **OCR** como plano B, e soma total da remessa.
- **📄 Relatórios** – exportação em PDF.

## 🛠️ Tecnologias

| Uso | Biblioteca |
|---|---|
| Banco de dados | [Supabase](https://supabase.com) (`@supabase/supabase-js` v2) |
| Planilhas | SheetJS (`xlsx`) |
| PDF | html2pdf.js |
| Leitura de QR Code | html5-qrcode |
| OCR | Tesseract.js (idioma `por`) |
| Ícones | Font Awesome |

Tabelas utilizadas no Supabase: `funcionarios`, `atas`, `eventos`, `acolhidos`, `patrimonio`.

## 🚀 Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/MichaelBorba/NOME-DO-REPOSITORIO.git
   ```
2. Crie um projeto no [Supabase](https://supabase.com) e as tabelas listadas acima.
3. No arquivo `index.html`, ajuste `SUPABASE_URL` e `SUPABASE_KEY` com os dados do seu projeto.
4. Abra o `index.html` no navegador ou publique com o **GitHub Pages** (*Settings → Pages*).

## 🔐 Segurança

- Use apenas a chave **anon** do Supabase no front-end (nunca a `service_role`).
- Ative **Row Level Security (RLS)** em todas as tabelas, pois a chave fica visível no navegador.
- O painel contém dados pessoais de funcionários e acolhidos: mantenha o acesso restrito e em conformidade com a LGPD.

## 🗺️ Próximos passos

- [ ] Concluir os módulos de Relatórios e D.P.
- [ ] Tela de login com perfis de acesso
- [ ] Separar CSS e JavaScript em arquivos próprios

## 👤 Autor

**Michael Borba** – [@MichaelBorba](https://github.com/MichaelBorba)
