## <B>MER</B> (Modelo Entidade-Relacionamento) e <B>DER</B> (Diagrama Entidade-Relacionamento)

- Prof. Marcelo Gonçalves de Souza

### Cardinalidades 1 (um) para 1 (um)

<p align="center">
  <img src="assets/img/conceitual_max11_0101.png" alt="Texto Alternativo" width="75%">
</p>

### No modelo lógico pode-se interpretar de duas formas:

1. Usa-se a regra do um para muitos:

- Motorista (<b>id</b>, nome, cnh)
- Veiculo (<b>id</b>, marca, modelo, placas, @id_motorista)<br />
      id_motorista referencia Motorista (id)

2. Usa-se uma tabela única

- Motorista_veiculo (<b>id</b>, nome, cnh, marca, modelo, placas)

### No modelo físico:

```
CREATE TABLE motorista(
  id BIGINT AUTO_INCREMENT,
  nome VARCHAR(128),
  cnh VARCHAR(128),
  PRIMARY KEY (id)
);
```
```
CREATE TABLE veiculo(
  id BIGINT AUTO_INCREMENT,
  marca VARCHAR(32),
  modelo VARCHAR(64),
  placas VARCHAR(16),
  id_motorista BIGINT,
  FOREIGN KEY (id_motorista) REFERENCES motorista (id)
  PRIMARY KEY (id)
);
```