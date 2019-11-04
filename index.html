<?php
//ini_set("display_errors", 1);
//ini_set("track_errors", 1);
//ini_set("html_errors", 1);
//error_reporting(E_ALL);

//The following script is tested only with servers running on Minecraft 1.7.

$SERVER_IP = "sky.freecraft.eu"; //Insert the IP of the server you want to query. 
$SERVER_PORT = "25555"; //Insert the PORT of the server you want to ping. Needed to get the favicon, motd, players online and players max. etc
$QUERY_PORT = "25555"; //Port of query.port="" in your server.properties. Needed for the playerlist! Can be the same like the port or different. Query must be enabled in your server.properties file!

$HEADS = "3D"; //"normal" / "3D"
$show_max = "unlimited"; // how much playerheads should we display? "unlimited" / "10" / "53"/ ...
$SHOW_FAVICON = "on"; //"off" / "on"

$TITLE = "My fancy Serverpage";
$TITLE_BLOCK_ONE = "General Information";
$TITLE_BLOCK_TWO = "Players";

////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

$ping = json_decode(file_get_contents('http://api.minetools.eu/ping/' . $SERVER_IP . '/' . $SERVER_PORT . ''), true);
$query = json_decode(file_get_contents('http://api.minetools.eu/query/' . $SERVER_IP . '/' . $QUERY_PORT . ''), true);

//Put the collected player information into an array for later use.
if(empty($ping['error'])) { 
	$version = $ping['version']['name'];
	$online = $ping['players']['online'];
	$max = $ping['players']['max'];
	$motd = $ping['description'];
	$favicon = $ping['favicon'];
}

if(empty($query['error'])) {
	$playerlist = $query['Playerlist'];
}

?>
<!DOCTYPE html>
<html>
	<head>
        <meta charset="utf-8">
        <title><?php echo htmlspecialchars($TITLE); ?></title>
        <link rel="stylesheet" href="https://netdna.bootstrapcdn.com/twitter-bootstrap/2.3.2/css/bootstrap-combined.no-icons.min.css">
    	<link href='http://fonts.googleapis.com/css?family=Lato:300,400' rel='stylesheet' type='text/css'>
    	<link href="https://netdna.bootstrapcdn.com/font-awesome/3.2.1/css/font-awesome.css" rel="stylesheet">
    	<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>
    	<script type="text/javascript" src="https://netdna.bootstrapcdn.com/twitter-bootstrap/2.3.2/js/bootstrap.min.js"></script>
    	<script language="javascript">
   		jQuery(document).ready(function(){
 			$("[rel='tooltip']").tooltip();
     	});
		</script>
    	<style>
    	/*Custom CSS Overrides*/
    	body {
      		font-family: 'Lato', sans-serif !important;
    	}
    	</style>
    </head>
    <body>
	<div class="container">
        <h1><?php echo htmlspecialchars($TITLE); ?></h1><hr>       
		<div class="row">
			<div class="span4">
				<h3><?php echo htmlspecialchars($TITLE_BLOCK_ONE); ?></h3>
				<table class="table table-striped">
					<tbody>
						<tr>
							<td><b>IP</b></td>
							<td><?php echo $SERVER_IP; ?></td>
						</tr>
					<?php if(empty($ping['error'])) { ?>
						<tr>
							<td><b>Version</b></td>
							<td><?php echo $version; ?></td>
						</tr>
					<?php } ?>
					<?php if(empty($ping['error'])) { ?>
						<tr>
							<td><b>Players</b></td>
							<td><?php echo "".$online." / ".$max."";?></td>
						</tr>
					<?php } ?>
						<tr>
							<td><b>Status</b></td>
							<td><?php if(empty($ping['error'])) { echo "<i class=\"icon-ok-sign\"></i> Server is online"; } else { echo "<i class=\"icon-remove-sign\"></i> Server is offline";}?></td>
						</tr>
					<?php if(empty($ping['error'])) { ?>
					<?php if(!empty($favicon)) { ?>
					<?php if ($SHOW_FAVICON == "on") { ?>
						<tr>
							<td><b>Favicon</b></td>
							<td><img src='<?php echo $favicon; ?>' width="64px" height="64px" style="float:left;"/></td>
						</tr>
					<?php } ?>
					<?php } ?>
					<?php } ?>
					</tbody>
				</table>
			</div>
			<div class="span8" style="font-size:0px;">
				<h3><?php echo htmlspecialchars($TITLE_BLOCK_TWO); ?></h3>
				<?php
				if($HEADS == "3D") {
					$url = "https://cravatar.eu/helmhead/";
				} else {
					$url = "https://cravatar.eu/helmavatar/";
				}

				if(empty($query['error'])) {
					if($playerlist != "null") { //is at least one player online? Then display it!
						$shown = "0";
						foreach ($playerlist as $player) {
							$shown++;
							if($shown < $show_max + 1 || $show_max == "unlimited") {
						?>
								<a data-placement="top" rel="tooltip" style="display: inline-block;" title="<?php echo $player;?>">
								<img src="<?php echo $url.$player;?>/50" size="40" width="40" height="40" style="width: 40px; height: 40px; margin-bottom: 5px; margin-right: 5px; border-radius: 3px; "/></a>
					<?php 	}
						}
						if($shown > $show_max && $show_max != "unlimited") {
							echo '<div class="span8" style="font-size:16px; margin-left: 0px;">';
							echo "and " . (count($playerlist) - $show_max) . " more ...";
							echo '</div>';
						}
					} else {
						echo "<div class=\"alert\" style=\"font-size:16px;\"> There are no players online at the moment!</div>";
					}
				} else {
					echo "<div class=\"alert\" style=\"font-size:16px;\"> Query must be enabled in your server.properties file!</div>";
				} ?>
			</div>
		</div>
	</div>
	</body>
</html>
