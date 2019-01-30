import 'package:flutter/material.dart';


void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp();

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Band Name Survey',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: const MyHomePage(title: 'Possible Band Names'),
    );
  }
}

class MockBandInfo {
  const MockBandInfo({this.name, this.votes});

  final String name;
  final int votes;
}

class MyHomePage extends StatelessWidget {
  const MyHomePage({Key key, this.title}) : super(key: key);

  static const List<MockBandInfo> _bandList = [
    const MockBandInfo(name: 'Name 1', votes: 1),
    const MockBandInfo(name: 'Name 2', votes: 2),
    const MockBandInfo(name: 'Name 3', votes: 3),
    const MockBandInfo(name: 'Name 4', votes: 4),
  ];

  final String title;

  Widget _buildListItem(BuildContext context, MockBandInfo bandInfo) {
    return ListTile(
      title: Row(
        children: [
          Expanded(
            child: Text(
              bandInfo.name,
              style: Theme.of(context).textTheme.headline,
            ),
          ),
          Container(
            decoration: const BoxDecoration(
              color: Color(0xffddddff),
            ),
            padding: const EdgeInsets.all(10.0),
            child: Text(
              bandInfo.votes.toString(),
              style: Theme.of(context).textTheme.display1,
            ),
          ),
        ],
      ),
      onTap: () {
        print('Should increase votes here');
      },
    );
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(title),
      ),
        body: ListView.builder(
          itemExtent: 80.0,
          itemCount: _bandList.length,
          itemBuilder: (context, index) =>
              _buildListItem(context, _bandList[index]),
        ),
    );
  }
}
