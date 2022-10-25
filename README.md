Enodes bootnodes = new Enodes();
bootnodes.append(new Enode("enode://a24ac7c5484ef4ed0c5eb2d36620ba4e4aa13b8c84684e1b4aab0cebea2ae45cb4d375b77eab56516d34bfbd3c1a833fc51296ff084b770b94fb9028c4d25ccf@52.169.42.101:30303"));

NodeConfig config = new NodeConfig();
config.setBootstrapNodes(bootnodes);
config.setEthereumNetworkID(4);
config.setEthereumGenesis(genesis);
config.setEthereumNetStats("yournode:Respect my authoritah!@stats.rinkeby.io");

Node node = new Node(getFilesDir() + "/.rinkeby", config);
node.start();
