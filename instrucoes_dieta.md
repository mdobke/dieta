# Instruções para Adicionar Nova Semana de Dieta ao HTML

Este documento explica como adicionar uma nova semana de dieta ao arquivo `dieta_semanal.html`. O objetivo é manter o formato moderno, divertido e interativo com ícones.

## Fluxo de Trabalho para Adicionar uma Nova Semana

Sempre que um novo arquivo de dieta (PDF) for fornecido, siga os passos abaixo:

1.  **Ler o Novo Arquivo PDF:**
    *   Utilize uma ferramenta de leitura de PDF (como a que foi usada para gerar este HTML) para extrair o texto do novo arquivo PDF.
    *   Analise o conteúdo para entender a estrutura da dieta (dias da semana, refeições, itens alimentares, quantidades, etc.) e quaisquer novas orientações ou receitas.

2.  **Extrair Informações da Dieta:**
    *   Organize as informações da nova semana de dieta em um formato estruturado, similar ao que foi feito para as Semanas 1 e 2.
    *   Identifique claramente os itens de cada refeição para cada dia da semana.
    *   Anote quaisquer novas receitas que não estejam presentes na seção de receitas existente.

3.  **Atualizar o Arquivo `dieta_semanal.html`:**

    *   **Adicionar uma Nova Aba (Tab) para a Semana:**
        *   Localize a seção `<ul class="nav nav-tabs" id="myTab" role="tablist">` no `dieta_semanal.html`.
        *   Adicione um novo `<li>` com um `button` para a nova semana. Certifique-se de que o `id` do botão e o `data-bs-target` sejam únicos (ex: `week3-tab`, `#week3`).
        *   Exemplo:
            ```html
            <li class="nav-item" role="presentation">
                <button class="nav-link" id="week3-tab" data-bs-toggle="tab" data-bs-target="#week3" type="button" role="tab" aria-controls="week3" aria-selected="false">Semana 3 <i class="fas fa-calendar-plus"></i></button>
            </li>
            ```

    *   **Adicionar o Conteúdo da Nova Semana:**
        *   Localize a seção `<div class="tab-content" id="myTabContent">`.
        *   Adicione um novo `<div class="tab-pane fade" id="weekX" role="tabpanel" aria-labelledby="weekX-tab">` (substitua `weekX` pelo ID da sua nova semana).
        *   Dentro deste `div`, adicione:
            *   Um `<h2>` com o título da semana (ex: `Dieta da Semana 3`).
            *   Uma seção de orientações (`<div class="orientations-section">`) com as orientações específicas para esta semana, seguindo o formato existente.
            *   Um novo acordeão (`<div class="accordion mt-4" id="accordionWeekX">`) para os dias da semana.

    *   **Adicionar os Dias da Semana no Acordeão:**
        *   Para cada dia da semana (Segunda-feira a Domingo), adicione um novo `accordion-item` dentro do acordeão da nova semana.
        *   Siga a estrutura existente para cada dia:
            *   `accordion-header` com um `button` (com `id` e `data-bs-target` únicos para o dia, ex: `headingW3Mon`, `#collapseW3Mon`).
            *   `accordion-collapse` com um `accordion-body`.
            *   Dentro do `accordion-body`, liste as refeições (`<div class="meal-time">`) e seus respectivos itens (`<ul><li>`).
            *   Utilize os ícones do Font Awesome para cada refeição e item, mantendo a consistência.

    *   **Atualizar a Seção de Receitas (se houver novas):**
        *   Se o novo PDF contiver receitas que ainda não estão no `dieta_semanal.html`, adicione-as à seção `<div class="recipe-section">`.
        *   Crie um novo `recipe-card` para cada nova receita, seguindo o formato existente.

4.  **Verificar e Testar:**
    *   Abra o arquivo `dieta_semanal.html` em um navegador para garantir que a nova semana foi adicionada corretamente.
    *   Verifique se as abas e os acordeões estão funcionando como esperado.
    *   Confira se a formatação e os ícones estão consistentes.

Ao seguir estas instruções, você poderá expandir o plano de dieta de forma organizada e manter a qualidade visual e interativa do HTML.
