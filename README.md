### Hi there 👋

<!--
<?php if ( ! defined('BASEPATH')) exit('No direct script access allowed');

class Visualizacao extends CI_Controller {
 
	/**
	*
	* contar_visualizacao
	*
	* Verifica se o IP do visitante já visulizou o id da
	* tabela no dia atual, se não tiver nenhum registro,
	* adiciona. Retorna true se é a primeira visualização
	* do IP no dia e falso se já foi visualizado
	*
	* @param $string, int
	* @return boolean
	*
	**/
	public function contar_visualizacao($tabela,$id){
	 
		$ip = $this->session->userdata('ip_address');
		$data = date('Y-m-d');
		 
		$dados = array(
			'tabela' => $tabela,
			'id_registro' => $id,
			'ip' => $ip,
			'data' => $data
		);
		$this->db->where($dados);
		if($this->db->count_all_results('visualizacoes') == 0){
			$this->db->insert('visualizacoes',$dados);
			return true;
		}
		return false;
	 
	}
	
}
?>
-->
