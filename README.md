# Agente TCI - Manual de Processos

Um assistente inteligente para consulta e pesquisa no Manual de Processos da organização, desenvolvido para integração em SharePoint como Web Part.

## 📋 Descrição

O Agente TCI é uma interface web moderna e intuitiva que permite aos usuários pesquisar rapidamente informações específicas no manual de processos da empresa. Com sistema de busca inteligente e interface responsiva, facilita o acesso às informações organizacionais.

## ✨ Características

### Tela Inicial Acolhedora
- **Logo Animado**: Cubo 3D com animação de rotação contínua
- **Apresentação Clara**: Título impactante com descrição das funcionalidades
- **Cards Informativos**: Destaque dos recursos principais do sistema
- **Transição Suave**: Animação elegante ao iniciar a pesquisa

### Sistema de Busca Inteligente
- **Busca por Relevância**: Algoritmo que prioriza resultados mais pertinentes
- **Múltiplos Critérios**: Busca exata, por palavras individuais e proximidade de termos
- **Sugestões Rápidas**: Tags com pesquisas frequentes para facilitar o uso
- **Destacação de Termos**: Realce visual dos termos pesquisados nos resultados

### Interface Moderna
- **Design Responsivo**: Funciona perfeitamente em desktop, tablet e mobile
- **Visual Limpo**: Fundo branco com elementos bem contrastados
- **Animações Suaves**: Transições e efeitos hover profissionais
- **Modal de Detalhes**: Visualização expandida dos resultados

## 🚀 Funcionalidades

### 🔍 Busca Inteligente
- Pesquisa em tempo real no conteúdo do manual
- Sistema de relevância que ordena resultados por importância
- Busca flexível: aceita termos únicos ou frases completas
- Suporte a caracteres especiais e acentos

### 📊 Resultados Relevantes
- Exibição inicial de 1 resultado principal
- Botão "Ver mais" para expandir todos os resultados
- Informação de localização (página e seção)
- Preview do conteúdo com destaque dos termos

### ⚡ Interface Rápida
- Carregamento instantâneo da interface
- Animações CSS otimizadas
- Scroll suave na área de resultados
- Feedback visual em todas as interações

### 📱 Compatibilidade
- **SharePoint**: Integração nativa como Web Part
- **Responsivo**: Adaptação automática para diferentes tamanhos de tela
- **Cross-browser**: Compatível com navegadores modernos
- **Acessível**: Navegação por teclado e leitores de tela

## 📁 Estrutura do Projeto

```
agente-tci/
│
├── index.html              # Arquivo principal da aplicação
├── README.md              # Documentação do projeto
│
├── assets/                # Recursos estáticos (se aplicável)
│   └── manual-tci.pdf     # PDF do manual (opcional)
│
└── docs/                  # Documentação adicional
    └── instalacao.md      # Guia de instalação
```

## 🛠️ Instalação

### Pré-requisitos
- Ambiente SharePoint Online ou SharePoint Server
- Permissões para adicionar Web Parts
- Arquivo PDF do manual (opcional)

### Instalação no SharePoint

1. **Preparar o Arquivo**
   ```bash
   # Baixe o arquivo index.html
   # Certifique-se de que está completo com CSS e JavaScript
   ```

2. **Adicionar Web Part**
   - Vá para a página desejada no SharePoint
   - Clique em "Editar página"
   - Adicione uma Web Part "Incorporar"
   - Cole o conteúdo do arquivo HTML

3. **Configurar PDF (Opcional)**
   - Carregue o PDF do manual na mesma biblioteca
   - Nomeie como um dos formatos suportados:
     - `manual-tci.pdf`
     - `manual-processos.pdf`
     - `manual.pdf`

4. **Salvar e Publicar**
   - Salve a página
   - Publique para disponibilizar aos usuários

## 📖 Como Usar

### Primeira Utilização
1. **Tela de Boas-vindas**: Aparece automaticamente no primeiro acesso
2. **Conhecer Recursos**: Visualize os cards explicativos
3. **Começar Pesquisa**: Clique no botão azul para iniciar

### Realizando Pesquisas
1. **Digite o Termo**: Use o campo de pesquisa principal
2. **Sugestões Rápidas**: Ou clique em uma das tags sugeridas
3. **Visualizar Resultados**: Examine os resultados encontrados
4. **Detalhes**: Clique em qualquer resultado para ver o conteúdo completo

### Dicas de Pesquisa
- **Termos Específicos**: Use palavras como "cadastro", "aprovação", "documento"
- **Frases Completas**: Digite perguntas naturais como "como aprovar um processo"
- **Palavras-chave**: Combine termos relacionados para resultados mais precisos

## ⚙️ Configuração Avançada

### Personalizações Disponíveis

#### Cores e Visual
```css
/* Personalizar cor principal */
:root {
    --cor-principal: #3b82f6;
    --cor-secundaria: #1e40af;
}
```

#### Lista de PDFs
```javascript
// Adicionar novos nomes de arquivos PDF
const possiblePdfNames = [
    'manual-tci.pdf',
    'manual-processos.pdf',
    'seu-manual.pdf'  // Adicione aqui
];
```

#### Sugestões de Pesquisa
```javascript
// Personalizar tags de sugestão
<button class="tci-suggestion-tag" onclick="searchSuggestion('seu-termo')">
    Seu Termo
</button>
```

## 🔧 Solução de Problemas

### Problemas Comuns

#### PDF não está carregando
- ✅ Verifique se o arquivo PDF está na mesma pasta
- ✅ Confirme se o nome do arquivo está na lista suportada
- ✅ Teste com um PDF menor primeiro

#### Interface cortada no SharePoint
- ✅ Verifique se está usando Web Part "Incorporar"
- ✅ Ajuste a altura da Web Part se necessário
- ✅ Teste em diferentes navegadores

#### Pesquisa não funciona
- ✅ Verifique se há erros no console do navegador
- ✅ Teste com termos mais simples
- ✅ Confirme se o JavaScript está habilitado

### Logs e Depuração
```javascript
// Verificar se PDF foi carregado
console.log('PDF carregado:', pdfLoaded);
console.log('Dados do PDF:', pdfData.length, 'seções');
```

## 📊 Especificações Técnicas

### Tecnologias Utilizadas
- **HTML5**: Estrutura semântica moderna
- **CSS3**: Animações, Grid Layout, Flexbox
- **JavaScript ES6+**: Funcionalidades interativas
- **PDF.js**: Processamento de arquivos PDF
- **SharePoint API**: Integração nativa

### Performance
- **Carregamento**: < 2 segundos para inicialização
- **Busca**: < 500ms para resultados simulados
- **PDF**: Processamento assíncrono para não bloquear interface
- **Memória**: Aproximadamente 2-5MB para PDFs médios

### Compatibilidade
- **Navegadores**: Chrome 80+, Firefox 75+, Safari 13+, Edge 80+
- **SharePoint**: Online, 2019, 2016
- **Dispositivos**: Desktop, Tablet, Mobile
- **Resolução**: 320px+ (mobile-first)

## 🤝 Contribuição

### Como Contribuir
1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas mudanças (`git commit -am 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

### Diretrizes
- Mantenha a consistência do código
- Teste em diferentes navegadores
- Atualize a documentação quando necessário
- Siga as convenções de nomenclatura existentes

## 📄 Licença

Este projeto está sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

R: Sim! O código é modular e pode ser adaptado para diferentes fontes de dados.

---
