# brasilprev

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>br.sp.vlira</groupId>
  <artifactId>brasilprev1</artifactId>
  <version>0.0.1-SNAPSHOT</version>

  <dependencies>
	 	<dependency>
			<groupId>io.cucumber</groupId>
			<artifactId>cucumber-java</artifactId>
			<version>6.1.2</version>
		</dependency>  
		<dependency>
			<groupId>info.cukes</groupId>
			<artifactId>cucumber-junit</artifactId>
			<version>1.2.6</version>
			<type>pom</type>
			<scope>test</scope>
		</dependency>
	</dependencies>
</project>


---------------------------------------------------------------------------------

https://centraldeajuda.brasilprev.com.br/categoria/orientacoes-gerais

 # language: pt
 
 Funcionalidade: Consulta de Cliente pelo CPF
    Como Consulta de Cliente por CPF
    Eu quero confirmar um cliente CPF = 11 digitos(alfa numericos) 
    Para saber se o mesmo esta cadastrado CPF
    
 Cenario: Não deve executar especificação
 		Dado que o valor do CPF = [134.546.567-36] 
 		Quando encrementar em = [12 digitos]
    Então o valor do  CPF = Erro    
 
  Cenario: Não deve executar especificação
 		Dado que o valor do CPF = [11 digitos]
 		Quando encrementar em = [12M.5%$.&86*76]
    Então o valor do  CPF = Erro  
 
 Cenario: Não deve executar especificação
 		Dado que o valor do CPF = [11 digitos]
 		Quando encrementar em = [666.777.666.99]
    Então o valor do  CPF = Erro    
 
 Funcionalidade: Consulta de Cliente pelo DDD e Telefone
    Como Consulta de Cliente por DDD e Telefone
    Eu quero confirmar um cliente pelo DDD e telefone 
    Para saber se o mesmo esta cadastrado CPF
       
Cenario: Deve executar especificação
 		Dado que o valor do DDD e do Telefone = [0-9]
 		Quando encrementar em = [011 - 876548756]
    Então o valor do  DDD e do Telefone = 011
    
Cenario: Não deve  incrementar Nova consulta
		Dado que o valor do DDD e do Telefone = [0-9]
 		Quando encrementar em = [0M0 - 76543RGRH]
    Então o valor do  DDD e do Telefone = erro
    
Cenario: Deve incrementar Nova consulta
 		Dado que o valor do DDD e do Telefone = [0-9]
 		Quando encrementar em = [021 - 65543347]
    Então o valor do  DDD e do Telefone = [021]
    
----------------------------------------------------------------------

package brasilprev1;

import static org.junit.Assert.assertArrayEquals;
import static org.junit.Assert.assertTrue;

import io.cucumber.java.en.Given;
import io.cucumber.java.en.Then;
import io.cucumber.java.en.When;
import junit.framework.Assert;

public class ConsultaDDDTelefone {
	@Given("que o DDD e Telefone est?o corretos = digitos alfa numerico")
	public void que_o_ddd_e_telefone_est_o_corretos_digitos_alfa_numerico() {
	    digitos = Alfa numericos
	}

	@Then("deve consultar o telefone com sucesso")
	public void deve_consultar_o_telefone_com_sucesso() {
	    // Write code here that turns the phrase above into concrete actions
		 digitos = Alfa numericos
	}

	@Given("que o DDD e Telefone ? numerico = digitos alfa numerico")
	public void que_o_ddd_e_telefone_numerico_digitos_alfa_numerico() {
		digitos = Alfa numericos
	}

	@Then("dever? exibir erro no DDD")
	public void dever_exibir_erro_no_ddd() {
	    assert.assertArrayEquals(message, expecteds, actuals, delta);(expected, atual);
}


  
