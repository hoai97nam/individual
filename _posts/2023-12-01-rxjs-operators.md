---
layout: post
title: Most common rxjs operators
subtitle: Most common rxjs operators can be misunderstood
published: true
comment: true
tags: [rxjs, operators]
gh-badge: [star, fork, follow]
permalink: /post/
---
## Most common rxjs operators

We will not separate into groups, this is sorted as ascending

# Table of Contents
1. [CombineLatest](#combineLatest)
2. [Concat](#concat)
3. [Merge](#merge)
4. [WithLatestFrom](#withLatestFrom)
5. [From](#from)
6. [CatchError](#catch)
7. [Filter](#filter)
7. [TakeUntil](#takeUntil)
8. [Share](#share)
9. [ShareReplay](#shareReplay)

### combineLatest: 
adapts Array<Observable> as input, will emit a value when obseravble elements (children observables) have at least 1 inner emission of each (children observables need for completion) and **in order**
 
 ![combineLatest]({{site.baseurl}}/img/combineLatest.png)

### concat:
combine multiple observables, but you want their emissions to be **in a specific order**, one after the other. children observables will emit only the previous one has completed.
 ![concat.png]({{site.baseurl}}/img/concat.png)
### merge:
  combines output of independent observable into a single stream. Emit values as soon as any of the observables emit a value (different from combineLatest or withLatestFrom).
  ![merge.png]({{site.baseurl}}/img/merge.png)
### withLatestFrom:
  Where the primary observable takes the lead and other observables chime in with their most recent values. `withLatestFrom` only emits a value when the main observable emits, and after each additional observable has emitted at least once.
  ![withLatestFrom.png]({{site.baseurl}}/img/withLatestFrom.png)
### from:
  - convert a promise to an observable
  - convert arrays and iterables as a sequence
### catch:
  Catches errors on the observable and return a new observable or throwing an error.
![catch.png]({{site.baseurl}}/img/catch.png)

### filter:
  filter will emit values that meet the specified condition. If no values in the observable satisfy the condition, nothing gets
![filter.png]({{site.baseurl}}/img/filter.png)

### takeUntil:
  use other emission to unsubcribe main observable
![takeUntil.png]({{site.baseurl}}/img/takeUntil.png)

### share:
  returns an Observable that mirrors the source. Omitted to side effect in `tap` operator

### shareReplay:
  subscribers to a stream that need access to previously emitted values. See similar `ReplaySubject`

### concatMap:
  returns an Observable that emits items based on applying a function supplying to each item emitted by the source Observable. Each new inner Observable is concatenated with the previous inner Observable

  Giống với mergeMap() và switchMap(), concatMap() cũng nhận vào 1 projectFunction và projectFunction này cũng sẽ phải trả về 1 Inner Observable. Khác với mergeMap() và switchMap(), concatMap() sẽ subscribe vào Inner Observable và sẽ CHỜ cho đến khi Inner Observable này complete thì mới subscribe vào Inner Observable tiếp theo (nếu như có Inner Observable tiếp theo). Chúng ta sẽ tiếp tục phân tích lại ví dụ ở trên nhé
![concatMap.png]({{site.baseurl}}/img/concatMap.png)
### map:
  apply projection with each value from source.
### mergeMap:
  mergeMap() cũng nhận vào 1 projectFunction mà sẽ nhận giá trị được emit từ Outer Observable và sẽ phải trả về 1 Inner Observable. Sau đó, mergeMap() sẽ subscribe Inner Observable này. Outer Observable + mergeMap() cuối cùng sẽ emit giá trị mà Inner Observable emit. mergeMap sẽ subscribe cùng lúc nhiều inner observable
![mergeMap.png]({{site.baseurl}}/img/mergeMap.png)

### switchMap:
  switchMap() sẽ unsubscribe Inner Observable nếu như Inner Observable đang được subscribe chưa complete MÀ Outer Observable lại emit tiếp.
![switchMap.png]({{site.baseurl}}/img/switchMap.png)
