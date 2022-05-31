# React 18

> React 18의 도래! React 블로그의 React18 소개 글 및 외부 문서를 요약한 것입니다.
>
> 출처: https://reactjs.org/blog/2022/03/29/react-v18.html





## 1. Concurrent React

 블로그에서 가장 처음으로 언급하는 지점입니다. 리액트의 렌더링 모델에 관여하는 behind-the-scenes mechanism이라서 우리 같은 웹 개발자에게는 그 정확한 원리는 중요하지 않을 수 있지만 그것이 사용자 경험에 어떠한 영향을 줄수 있을지는 고민해야 할 것입니다. 

 가장 처음으로 언급하는 feature는 렌더링이 interruptible해진다는 것입니다. 예컨대 중요한 작업(urgent)(ex) 유저의 클릭, 타이핑 등)이 덜 중요한 작업(ex) 검색 결과 표출)에 의한 렌더링 중간에 interrupt하여 사용자 경험을 더욱 매끄럽게 만들어줄 수 있습니다. `useTransition`과 같은 새로 도입되는 hook으로 더 원활하게 지원될 것입니다. 또, hydration 과정에서 사용자가 상호작용을 원하는 컴포넌트의 코드를 우선 불러올 수도 있게 될 것입니다.

 두 번째로 언급하는 feature는 reusable state입니다. 예컨대 섹션을 제거했다가 다시 스크린에 띄워도 이전의 state를 그대로 쓸 수 있게 되는 것이죠. 이는 아직 도입되지는 않은 새로운 컴포넌트 `<Offscreen>`로 활용할 수 있는데요, 새로운 UI를 백그라운드에서 준비하여 더 원활한 사용자 경험을 제공할 수 있을 것입니다.





## 2. Server Components

여전히 개발 중이긴 합니다. 18.1.0에서도 여전히 experimental로 체크되어 있는 것을 보니 아직은 사용할 수 없을 듯합니다. 서버사이드렌더링으로 비약적인 성능의 향상을 불러올 수 있는 혁신적인 기능이나 아직 도입되지는 않았으므로 추후 보강하겠습니다.





## New Features



### Automatic Batching

 이제 onClick과 같은 react 이벤트에서 말고도 timeouts, promises, native event handlers와 같은 맥락에서도 Automatic Batching을 이용할 수 있습니다! 렌더링에 따른 부담을 줄여 더 나은 성능을 보여줄 수 있는 것이지요.



### Suspense

 기존에도 존재하긴 했으나 client side에서 code split 등의 한정적인 용도로밖에 쓰이지 않았습니다. server side에서도 본격적인 지원이 시작됩니다. 아직 아쉽게도 HTML 스트리밍은 지원되지 않지만요.
