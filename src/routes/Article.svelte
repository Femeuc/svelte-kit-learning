<script lang='ts'>
    import { onMount } from 'svelte';

    let article: HTMLElement;
    let children_with_text: Element[] = [];

    onMount(async () => {
		set_children_with_text(article);
	});

    function set_children_with_text( element: Element ): void {
        if(element.childElementCount) {
            for (const child of element.children) {
                set_children_with_text(child);
            }
            return;
        }          
        children_with_text.push(element);
    }

    function hide_text(): void {
        let text: String = '';
        children_with_text.forEach( child => {
            text = child.textContent ? child.textContent: '';
            const words = text.split(' ');

            child.innerHTML = '';
            words.forEach( w => {
                child.innerHTML += `<span class="word hidden">${w}</span>`;
            });
        });
    }
</script>

<article  bind:this={article}>
        <h1>Reino dos Países Baixos</h1>
        <p>O Reino dos Países Baixos (em neerlandês: Koninkrijk der Nederlanden AFI: [ˈkoːnɪŋkrɛiɡ dɛr ˈneːdərlɑndə(n)] (Sobre este somescutar (ajuda·info))) é um Estado soberano que, desde 2010, é composto por quatro nações constituintes: os Países Baixos, na Europa; Aruba, Curaçau e São Martinho nas Caraíbas (Caribe em português brasileiro).    </p>
        <p>O Estatuto do Reino dos Países Baixos, datado de 1954, determina quais os assuntos geridos pelo reino. O monarca do Reino é também o monarca de cada um dos países, ou seja, o Rei Guilherme Alexandre dos Países Baixos e os seus herdeiros legítimos. O monarca encabeça o conselho regente executivo do reino e de cada um dos países, sendo representado por governadores em Curaçau, em Aruba e em São Martinho. Entre os assuntos geridos pelo reino encontram-se os relacionados com:    </p>
        <ul>
            <li>Defesa</li>
            <li>Relações exteriores e comércio exterior</li>
            <li>Cidadania</li>
            <li>Extradição</li>
        </ul>
        <p>Outros assuntos são delegados aos governos nacionais. O estatuto do Reino pôs fim à relação colonial entre os Países Baixos por um lado e as Antilhas Holandesas e o Suriname por outro. Em 25 de novembro de 1975, o Suriname declarou independência e, em 1986, Aruba conseguiu um estatuto separado das restantes ilhas das Caraíbas. Em 2010 houve a dissolução do que restava das antigas Antilhas Neerlandesas, sendo criados mais dois países, Curaçau e São Martinho, bem como foram anexadas aos Países Baixos, como municípios especiais, as ilhas de Bonaire, Santo Eustáquio e Saba.</p>
        <p>Cada um dos países tem um documento próprio descrevendo a formação do seu governo:</p>
        <ul>
            <li>a Constituição dos Países Baixos — a grondwet. Apesar de o seu título fazer alusão ao reino aplica-se apenas aos Países Baixos europeus.</li>    
            <li>a Constituição de Aruba — a staatsregeling de Aruba.</li>
            <li>a Constituição das Antilhas Neerlandesas — a staatsregeling das Antiilhas Neerlandesas, revogada em 2010.</li>
        </ul>
        <p>O conselho de ministros do reino é composto pelos ministros dos Países Baixos e um ministro plenipotenciário de cada um dos outros países.    </p>
        <p>Antes de 1954, o "Reino dos Países Baixos" referia-se aos Países Baixos e às suas colónias. Antes de 1830, formalmente em 1839, o Reino Unido dos Países Baixos incluía também, como países, a Bélgica e o Luxemburgo.
        </p>
        <p>O ponto mais alto do Reino é o monte Scenery, 862 metros de altitude, na ilha de Saba, no Caribe.    </p>

        <h2>Reestruturação do Reino dos Países Baixos
        </h2>
        <p>O Reino dos Países Baixos passou por um processo de reestruturação naquilo que se refere as Antilhas Holandesas, ou seja, as ilhas de Curaçau, São Martinho, Bonaire, Santo Eustáquio e Saba. Aruba manterá o mesmo estado de país dentro do reino.[2]  </p>
        <p>Essa reestruturação tem por base os referendos realizados em cada uma das ilhas das Antilhas Holandesas, entre 2000 e 2005, cujos resultados foram inequívocos: ao mesmo tempo que as ilhas não desejavam continuar a fazer parte das Antilhas Holandesas, elas também não queriam cortar os vínculos existentes com o Reino.   </p>
        <p>Na atual situação, o Reino é formado por quatro países em condições de igualdade: Aruba, Curaçau, São Martinho e os Países Baixos Europeus. Os territórios caribenhos do Reino não são considerados como territórios ultramarinos, e sim, países plenos e autônomos dos Países Baixos dentro do Reino. Os quatro países tem um alto grau de autonomia interna. As relações internacionais e de defesa são assuntos do Reino. O governo do Reino é formado pelo Conselho de Ministros, que se reúne em Haia e no qual cada país caribenho é representado por seu primeiro ministro. A sede do governo nacional de Curaçau encontra-se em Willemstad, a de Aruba, em Oranjestad e a de São Martinho em Philipsburg.   </p>
        <p>Na nova estrutura, a partir de outubro de 2010, as duas maiores ilhas das antigas Antilhas Holandesas, Curaçau e São Martinho, evoluíram para o status de país dentro do Reino, comparável ao que têm, atualmente, os Países Baixos e Aruba. O território das “Antilhas Holandesas” deixou de existir assim que a futura estrutura entrou em vigor. A partir de então, o Reino passou a ser composto por quatro países em vez de três: Países Baixos, Aruba, Curaçau e São Martinho. Quanto às três ilhas menores (Bonaire, São Eustáquio e Saba), elas passarão a ter um vínculo direto com os Países Baixos,se tornando municípios especiais. Na prática, sua condição será muito parecida à dos municípios europeus, salvo adaptações derivadas de sua localização nas Caraíbas.  </p>
        <p>A reforma política não terá impacto na manutenção dos interesses internacionais. Isso significa, dentre outros, que:</p>
        <ul>
            <li>não haverá alteração nas fronteiras exteriores do Reino;</li>
            <li>as relações internacionais, bem como a defesa, continuarão sendo assuntos do Reino;</li>
            <li>haverá apenas um único ministro das Relações Exteriores para todo o Reino, que arcará com a responsabilidade de todos os assuntos pertinentes à pasta;</li>
            <li>o Ministério de Relações Exteriores em Haia e suas representações no exterior continuarão trabalhando para o Reino e suas partes constituintes;</li>
            <li>apenas o Reino poderá celebrar tratados e não cada uma de suas partes constituintes em separado (embora sua vigência poderá limitar-se a uma ou várias partes constituintes do Reino, ou seja, o tratado celebrado pelo Reino poderá referir-se a uma ou mais partes constituintes do Reino).</li>
        </ul>

        <h2>Dados</h2>
        <table>
            <tr><th>País</th> <th>Capítal</th> <th>População</th> <th>Área (km²)</th> <th>Densidade</th></tr>
            <tr><td>Países Baixos</td>	<td>Amesterdão</td>	<td>16.570.613</td> <td>41.528</td>	<td>395</td></tr>
            <tr><td>Aruba</td>	<td>Oranjestad</td>	<td>103.062</td>	<td>180</td> <td>534</td></tr>
            <tr><td>Curaçau</td>	<td>Willemstad</td>	<td>173.400</td>	<td>444</td> <td>>391</td></tr>
            <tr><td>São Martinho</td>	<td>Philipsburg</td>	<td>37.429</td>	<td>34</td> <td>1.100</td></tr>
        </table>
</article>


<style>
    :root {
        --hidden-word: hsl(0, 0%, 50%);
    }
    article > * {
        margin-bottom: 10px;
    }
    ul {
        padding-left: 10px;
        list-style-position: inside;
    }
    table, th, td {
        border: 1px solid var(--text-color);
        padding: 5px 10px;
    }
    table {
        border-collapse: collapse;
    }
</style>