# Redundância e SLA na Nuvem Azure

Este documento tem como objetivo explicar de forma objetiva os conceitos de **redundância** e **SLA (Service Level Agreement)** no contexto da computação em nuvem com a Microsoft Azure.

---

## O que é Redundância?

Redundância é a prática de duplicar componentes ou sistemas para garantir **disponibilidade e continuidade de serviço**, mesmo em caso de falhas.

### Tipos de Redundância na Azure:

* **Redundância Local (LRS)**

  * Cópias dos dados são mantidas dentro do mesmo datacenter.
  * Protege contra falhas de hardware localizadas.

* **Redundância Geográfica (GRS)**

  * Cópias dos dados em uma região secundária distante.
  * Oferece maior proteção em desastres naturais ou indisponibilidades regionais.

* **Redundância de Zona (ZRS)**

  * Armazena os dados em zonas de disponibilidade distintas dentro de uma mesma região.
  * Alta disponibilidade para aplicativos de missão crítica.

### Benefícios:

* Previne perda de dados
* Garante continuidade dos serviços
* Suporta recuperação de desastres (Disaster Recovery)

---

## O que é SLA (Service Level Agreement)?

O SLA é um **acordo de nível de serviço** entre o provedor (ex: Microsoft) e o cliente, especificando a **disponibilidade mínima garantida** para um serviço.

### Exemplo de SLA na Azure:

* Azure App Service: **99,95% de disponibilidade**
* Azure SQL Database com redundância geográfica: **99,99%**

### Cálculo de Indisponibilidade Permitida:

| SLA (%) | Tempo máximo de indisponibilidade por mês |
| ------- | ----------------------------------------- |
| 99%     | \~7 horas e 18 minutos                    |
| 99,9%   | \~43 minutos                              |
| 99,99%  | \~4 minutos                               |
| 99,999% | \~26 segundos                             |

### Por que isso importa?

* Ajuda a escolher o **tipo de recurso e redundância** baseado na necessidade do negócio
* Garante que o serviço esteja disponível conforme prometido
* Em caso de não cumprimento, pode haver **créditos financeiros** de volta ao cliente

---

## Relação entre SLA e Redundância

* Quanto **maior o nível de redundância**, maior tende a ser o SLA.
* Uma aplicação crítica pode exigir **ZRS ou GRS** para atingir SLA de 99,99% ou superior.
* Redundância é uma das **estratégias principais para garantir alta disponibilidade**.

---

## Considerações Finais

Ao planejar um sistema na nuvem, é essencial:

* Compreender o nível de SLA oferecido
* Escolher a estratégia de redundância adequada
* Avaliar o custo-benefício de cada opção com base na criticidade do serviço

Utilizar bem esses conceitos pode evitar prejuízos com indisponibilidade e garantir uma experiência de usuário confiável e profissional.
