nomes-do-meio-em-minuscula
==========================

unção (PHP) que deixa o nome completo com as iniciais em caixa alta, com exceção dos "nomes do meio", como: da, de, do, das, dos...

<?php
//Função que deixa o nome completo com as iniciais em caixa alta, com exceção dos "nomes do meio", como: da, de, do, das, dos...

function nomesDoMeio($nome) {
	$nome = strtolower($nome);
	$nomeEmArray = explode(" ", $nome);

	$excessoes = array("da", "de", "do", "das", "dos");

	foreach ($nomeEmArray as $palavra) {
		if (in_array($palavra, $excessoes)) {
			echo $palavra . " ";
			continue;
		} else {
			echo ucwords($palavra . " ");
		}
	}
}

?>
