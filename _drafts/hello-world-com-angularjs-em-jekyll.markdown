---
layout: post
title: "Hello world com AngularJS em jekyll"
date: 2015-06-20T01:14:45-03:00
---

<script src="http://ajax.googleapis.com/ajax/libs/angularjs/1.2.19/angular.min.js"></script>
<script>
    var app = angular.module('angularDemo', []);

    app.config(function($interpolateProvider){
        $interpolateProvider.startSymbol('{[{').endSymbol('}]}');
    });

    app.controller('MainCtrl', function($scope){
        $scope.hello = 'Hello world!';
    });
</script>

<script src="https://gist.github.com/fhisamoto/66235c6c7f057e0ba829.js"></script>

<style>
    .ng-container {
        width: 200px;
        padding: 20px;
        text-align: center;
    }
</style>

<div ng-app="angularDemo" ng-controller="MainCtrl" class="ng-container">
    <h1>{[{hello}]}</h1>
</div>
