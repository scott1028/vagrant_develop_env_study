0.透過 vagrant box add precise32 http://files.vagrantup.com/precise32.box 下載虛擬機器原型(Ubuntu 12.04)
1.vagrant init 可於當前目錄產生 varantfile 虛擬機器配置文件
2.修改 vagrantfile 文件內根據 http://docs.vagrantup.com/v2/provisioning/shell.html 文檔說明內
	Vagrant.configure("2") do |config|
	  config.vm.provision "shell", path: "script.sh"
	end
	
	可以讓他自動跑 shell Script 可用來執行安裝套件腳本。
	
3.根據 http://docs.vagrantup.com/v2/synced-folders/index.html 文檔說明，/vagrant 目錄將是 client 與 host 端的同步資料夾！
4.有關 vagrant up 內執行過的 vagrantfile 內之 shell Script 安裝套件腳本，如果要重新執行就把 .vagrant 資料夾刪除即可！

