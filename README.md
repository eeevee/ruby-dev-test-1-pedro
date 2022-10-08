# ruby-dev-test-1

Desenvolver a camada de modelos de um sistema de arquivos persistido em um banco de dados SQL onde seja possível criar diretórios e arquivos. Os diretórios poderão conter sub-diretórios e arquivos. O conteúdo dos arquivos podem estar ser persistidos como blob, S3 ou mesmo em disco.

A soluçãos deverá ser escrita majoritariamente em Ruby com framework Ruby on Rails.

Realizar um fork deste repositório e abrir o PR ao finalizar.

Folder
    - parent_id
        - default nil
    - name

File
    - path
    - folder_id
    - type
        - blob, s3, localStorage

FolderService
    - create
        - parent_id
        - name
    - update
        - name only
    - delete
        - delete sub folders and files

FileService
    - create
        - type
            - strategy to create
        - file
        - folder_id
    - delete