# solid-with-php
Treinamento da plataforma Alura sobre SOLID aplicado ao PHP

Commit "Extraindo Feedback" : Utilizando o Single Responsability Principle, agora a classe Curso só tem um motivo 
para mudar e a classe Feedback também.

Commit "Extraindo a pontuação" : Aplica o Open Closed Principle, que dia que
uma entidade dedve ser aberto para expansão, porém fechadas para modificações.
Ou seja, no nosso caso, a classe CalculadorPontuacao iria crescer infinitamente, 
aumentando o número de ifs, a solução foi implementar a interface pontuável, onde teremos
a classe que implementá-lo com a responsabilidade de prover um método de cálculo da pontuação.

Commit "Corrigindo url" : Devemos respeitar as definições impostas pelas classes pai.
No caso da aplicação, deveríamos receber uma url na classe AluraMais, porém não iríamos recebê-la. Ou seja, viola o princípio da Substituição de Liskov.

Commit "Assistindo com simplicidade" : Devemos ficar atentos ao princípio de Inversão de Dependência, que nos diz que
classes concretas devem depender de abstrações e não o contrário.
No nosso caso tínhamos a classe Assistidor implementando duas maneiras diferentes para assistir. Bastava organizar
a responsabilidade, jogando para a classe a ser implementada o deve de assistir ao conteudo.

Commit "Separando as interfaces" : Uma interface não deve assumir responsabilidades que não é dela.
No nosso caso, a interface Pontuável não é obrigada a implementar o método assistir, pois pode haver situações que pontuem mas não sejam para assistir.
Por exemplo uma dúvida.