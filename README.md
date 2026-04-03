Passos para subir os recursos corretamente:

- Na Cloud: Start Lab > AWS Details > Colocar as credenciais no arquivo .aws (Procure no seu '/Users/...') > Salvar

- Crie uma chave PEM dentro do console da AWS 
    - EC2 > Pares de chaves > Nome de exemplo: urubu100-key

- Com a chave criada, coloque o nome dela no parâmetro `Ec2KeyPairName`, dentro do arquivo jupyerfinal.yaml

- Altere o nome dos buckets!!!!! (AWS não aceita nomes iguais de bucket)

- Rode o comando (no local em que está o arquivo .yaml)
```
aws cloudformation create-stack --stack-name last-mile-optimization-stack --template-body file://cloud-formation.yaml
```

- Vá no console em **Cloudformation** > **Pilhas** e verifique se a stack está com o status **CREATE_COMPLETE**


- Caso o arquivo seja alterado: Atualize a stack com o comando abaixo:
```
aws cloudformation update-stack --stack-name last-mile-optimization-stack --template-body file://cloud-formation.yaml
```

- Vá no console em **Cloudformation** > **Pilhas** e verifique se a stack está com o status **UPDATE_COMPLETE**




