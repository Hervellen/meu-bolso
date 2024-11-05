## foi utilizado typscript e next
 - Pasta App é a mais importante que é onde fica o page.tsx que é onde fica a visualização
 - sempre exportar a pasta com default para ela funcionar 
 - comando para abrir a sintaxe: sfc 
                    const = () =>{
                        return ()
                    }

                    export default;
        =================================
            const Transactions = () =>{
                return <h1>Transactions page</h1>;
            };

            export default Transactions;
    * as rotas serão criadas por pastas com o arquivo tsx
 - para ter acesso a páginas dentro da página precisa criar um [id] e a page.tsx (O next usa o nome da pasta entre colchetes para receber o parâmetro agregado a ele )   

- arquivo layout.tsx fica visível em todas as páginas

## Base de dados 
 - utiliza o prisma que é um ORM: facilita o seu trabalho com o banco de dados (ele escreve o código e integra com o typescript)
  - instalei o prisma e foi criado o banco no arquivo .env DATABASE_URL="postgresql://johndoe:randompassword@localhost:5432/mydb?schema=public"
  - no schema.prisma é que criamos as tabelas
  - id String @id @default(uuid()) é a geração de id aleatório
  - usar o neon console para rodar o postgres 
  - fazer a migrations para aplicar os comandos no banco: npx prisma migrate dev --name init_db

  ## Commit
  - fazer commit de cada passo do projeto
  - usar o Conventional Commits, com ele usa prefixos para identificar o tipo de commit, se foi para correção de um bug por exemplo
    git add .
    git commit -m "chore: add prisma and database setup"