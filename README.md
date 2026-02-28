# 🚀 Desafio Técnico — Metaobjects + Metafields no Shopify

## 📌 Nome do Desafio
Implementação de um **Slider Dinâmico de Produtos com Banner** utilizando **Metaobjects, Metafields e Liquid** no Shopify.

---

# 🧠 O que são Metafields?

Metafields são campos personalizados que permitem adicionar informações extras a recursos do Shopify (como Produtos, Coleções, Páginas etc).

Eles são usados quando precisamos armazenar dados que não existem por padrão no Shopify.

Exemplo:
- Informações técnicas extras
- Vídeos personalizados
- Produtos relacionados
- Listas personalizadas

Neste projeto, o metafield foi utilizado para armazenar uma **lista de metaobjects vinculados a um produto**.

---

# 🗂️ O que são Metaobjects?

Metaobjects são estruturas personalizadas criadas dentro do Shopify que funcionam como “mini bancos de dados”.

Eles permitem criar tipos de conteúdo reutilizáveis com múltiplos campos.

Exemplo:
- Banner + Produto
- Depoimento (nome + foto + texto)
- Bloco promocional
- FAQ customizado

Neste projeto, foi criado um metaobject contendo:
- 🖼️ Um banner (imagem)
- 🛍️ Um produto relacionado

---

# 🎯 O que foi Implementado

Foi desenvolvido:

✔️ Uma section customizada em Liquid  
✔️ Um slider usando Swiper.js (CDN)  
✔️ Integração dinâmica com Metaobjects  
✔️ Metafield de lista vinculado ao produto  
✔️ Renderização automática dos banners e produtos relacionados  

O conteúdo do slider pode ser gerenciado totalmente pelo Admin do Shopify, sem necessidade de alterar o código.

---

# ⚙️ Como Criar o Metaobject

1. Acesse:
   Settings → Custom Data → Metaobjects

2. Clique em **Add Definition**

3. Configure:
   - Name: Related Products with Banner
   - Type: related_products_with_banner

4. Adicione os campos:
   - banner → Tipo: File (Image)
   - product → Tipo: Product Reference

5. Salve.

---

# 🏷️ Como Criar o Metafield

1. Vá em:
   Settings → Custom Data → Products

2. Clique em **Add Definition**

3. Configure:
   - Name: Related Products with Banner
   - Namespace and Key:
     custom.related_products_with_banner
   - Type:
     Metaobject → List → Related Products with Banner

4. Salve.

---

# 🔗 Como Associar ao Produto

1. Vá em:
   Products → Abra um produto

2. Role até a seção de Metafields

3. No campo criado:
   - Selecione os metaobjects criados
   - Salve o produto

Se o campo não for preenchido, o slider não será exibido.

---

# 🧩 Implementação Técnica (Resumo)

A section criada realiza:

1. Busca do produto selecionado
2. Acesso ao metafield:
   selected_product.metafields.custom.related_products_with_banner
3. Loop nos metaobjects
4. Renderização dos dados no HTML
5. Inicialização do Swiper para transformar em slider

---

# 🖥️ Como Testar Localmente

1. Instale o Shopify CLI
2. No terminal, execute:

   shopify theme dev

3. Acesse a URL local fornecida pelo CLI
4. Vá até uma página de produto
5. Adicione a section “Metaobject Slider”
6. Selecione um produto configurado

Certifique-se de que:
- O metafield esteja preenchido
- O Swiper CDN esteja importado no theme.liquid

---

# 🔀 Pull Request

Link do Pull Request:

👉 

---

# 🎥 Vídeo Explicativo

Link do vídeo demonstrando a implementação:

👉 https://drive.google.com/file/d/1iQ6bhg6oYQKsaWgDQm1u91A5wIdN32j7/view?usp=drive_link

---

# ✅ Resultado Final

- Slider dinâmico funcional
- Integração com Metaobjects
- Estrutura escalável
- Gerenciamento via Admin
- Implementação limpa em Liquid
