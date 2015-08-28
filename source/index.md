---
title: API Reference

language_tabs:
  - JSON

toc_footers:
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to Careerfully API!

# Authentication

# APIs

## Users
Method | Path | Params 
-------------- | -------------- | --------------
POST | /users/create | email, password, full_name

## Session
Method | Path | Params 
-------------- | -------------- | --------------
POST | /sessions/create | email, password
DELETE | /sessions/destroy | 

## Matches
Method | Path | Params 
-------------- | -------------- | --------------
GET | /matches/index | 
GET | /matches/show | id

## Applications
## Profile