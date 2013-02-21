PHP File Database
====================

A tiny class to store PHP arrays into JSON files


Example
--------------------

<pre>// Create a new instance for mydatabase.json
$fdb = new FileDatabase('mydatabase');

// Read the database
$db = $fdb->get();

// If it doesn't exist, we create it
if (!$db) {$db = array();}

// Add some data (treat it as an associative array)
$db['name'] = 'Xavi';
$db['lastupdate'] = 1361481412;
$db['colors'] = array(
	'main' => '#39123f',
	'success' => '#bec531',
	'error' => '#ec008c'
);

// Now save it back
$db = $fdb->set($db);</pre>


Performance note
--------------------

PHP File Database is great when you need to store information but a MySQL database would be too much of a hassle. If you are working with a lot of data or need to do complex queries, an SQL database is the way to go.