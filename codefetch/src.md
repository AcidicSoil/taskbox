src/App.css
```
1 | #root {
2 |   max-width: 1280px;
3 |   margin: 0 auto;
4 |   padding: 2rem;
5 |   text-align: center;
6 | }
7 | 
8 | .logo {
9 |   height: 6em;
10 |   padding: 1.5em;
11 |   will-change: filter;
12 |   transition: filter 300ms;
13 | }
14 | .logo:hover {
15 |   filter: drop-shadow(0 0 2em #646cffaa);
16 | }
17 | .logo.react:hover {
18 |   filter: drop-shadow(0 0 2em #03a1fc);
19 | }
20 | 
21 | @keyframes logo-spin {
22 |   from {
23 |     transform: rotate(0deg);
24 |   }
25 |   to {
26 |     transform: rotate(360deg);
27 |   }
28 | }
29 | 
30 | @media (prefers-reduced-motion: no-preference) {
31 |   a:nth-of-type(2) .logo {
32 |     animation: logo-spin infinite 20s linear;
33 |   }
34 | }
35 | 
36 | .card {
37 |   padding: 2em;
38 | }
39 | 
40 | .read-the-docs {
41 |   color: #888;
42 | }
```

src/App.tsx
```
1 | import "./index.css";
2 | import store from "./lib/store";
3 | 
4 | import { Provider } from "react-redux";
5 | import InboxScreen from "./components/InboxScreen";
6 | 
7 | function App() {
8 |   return (
9 |     <Provider store={store}>
10 |       <InboxScreen />
11 |     </Provider>
12 |   );
13 | }
14 | export default App;
```

src/index.css
```
1 | * {
2 |   box-sizing: border-box;
3 |   -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
4 |   -webkit-tap-highlight-color: transparent;
5 | }
6 | 
7 | html,
8 | body {
9 |   margin: 0;
10 |   padding: 0;
11 |   font-size: 100%;
12 |   outline: none;
13 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
14 |   font-style: 400;
15 |   color: #333;
16 |   font-size: 16px;
17 |   background-color: #26c6da;
18 |   -webkit-text-size-adjust: 100%;
19 |   -ms-text-size-adjust: 100%;
20 |   -webkit-font-smoothing: antialiased;
21 |   -moz-osx-font-smoothing: grayscale;
22 | }
23 | 
24 | h1,
25 | p,
26 | label {
27 |   margin: 0;
28 |   padding: 0;
29 |   border: 0;
30 |   font-weight: normal;
31 |   font-style: normal;
32 |   font-size: 100%;
33 |   line-height: 1;
34 |   font-family: inherit;
35 |   vertical-align: baseline;
36 |   vertical-align: middle;
37 |   line-height: normal;
38 |   overflow: visible;
39 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
40 | }
41 | 
42 | button::-moz-focus-inner,
43 | input::-moz-focus-inner {
44 |   border: 0;
45 |   padding: 0;
46 | }
47 | 
48 | button,
49 | input[type="button"],
50 | input[type="reset"],
51 | input[type="submit"] {
52 |   cursor: pointer;
53 |   -webkit-appearance: button;
54 | }
55 | 
56 | @keyframes spin {
57 |   0% {
58 |     transform: rotate(0deg);
59 |   }
60 | 
61 |   100% {
62 |     transform: rotate(359deg);
63 |   }
64 | }
65 | 
66 | @keyframes glow {
67 |   0%,
68 |   100% {
69 |     opacity: 1;
70 |   }
71 | 
72 |   50% {
73 |     opacity: 0.5;
74 |   }
75 | }
76 | 
77 | @font-face {
78 |   font-family: "Nunito Sans";
79 |   font-style: italic;
80 |   font-weight: 400;
81 |   src: url(https://fonts.gstatic.com/s/nunitosans/v6/pe0oMImSLYBIv1o4X1M8cce4E9lKcw.ttf)
82 |     format("truetype");
83 | }
84 | 
85 | @font-face {
86 |   font-family: "Nunito Sans";
87 |   font-style: normal;
88 |   font-weight: 400;
89 |   src: url(https://fonts.gstatic.com/s/nunitosans/v6/pe0qMImSLYBIv1o4X1M8cce9I94.ttf)
90 |     format("truetype");
91 | }
92 | 
93 | @font-face {
94 |   font-family: "Nunito Sans";
95 |   font-style: normal;
96 |   font-weight: 800;
97 |   src: url(https://fonts.gstatic.com/s/nunitosans/v6/pe03MImSLYBIv1o4X1M8cc8aBc5tU1Q.ttf)
98 |     format("truetype");
99 | }
100 | 
101 | .type-light {
102 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
103 |   font-weight: 300;
104 | }
105 | 
106 | .type-bold {
107 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
108 |   font-weight: 800;
109 | }
110 | 
111 | .type-italic {
112 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
113 |   font-weight: 400;
114 |   font-style: italic;
115 | }
116 | 
117 | input[type="text"],
118 | input[type="email"],
119 | input[type="password"],
120 | textarea {
121 |   font-size: 14px;
122 |   line-height: 20px;
123 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
124 |   font-style: 400;
125 |   padding: 0.75rem 0;
126 |   line-height: 1.5rem !important;
127 |   border: none;
128 |   border-radius: 0;
129 |   box-sizing: border-box;
130 |   color: #333;
131 |   outline: none;
132 | }
133 | 
134 | .checkbox {
135 |   display: inline-block;
136 |   height: 3rem;
137 |   position: relative;
138 |   vertical-align: middle;
139 |   width: 44px;
140 | }
141 | 
142 | .checkbox input[type="checkbox"] {
143 |   font-size: 1em;
144 |   visibility: hidden;
145 | }
146 | 
147 | .checkbox input[type="checkbox"] + span:before {
148 |   position: absolute;
149 |   top: 50%;
150 |   right: auto;
151 |   bottom: auto;
152 |   left: 50%;
153 |   width: 0.85em;
154 |   height: 0.85em;
155 |   transform: translate3d(-50%, -50%, 0);
156 |   background: transparent;
157 |   box-shadow: #2cc5d2 0 0 0 1px inset;
158 |   content: "";
159 |   display: block;
160 | }
161 | 
162 | .checkbox input[type="checkbox"]:checked + span:before {
163 |   font-size: 16px;
164 |   line-height: 24px;
165 |   box-shadow: none;
166 |   color: #2cc5d2;
167 |   margin-top: -1px;
168 |   font-family: "percolate";
169 |   font-style: normal;
170 |   font-weight: normal;
171 |   font-variant: normal;
172 |   text-transform: none;
173 |   line-height: 1;
174 | 
175 |   content: "\e65e";
176 | }
177 | 
178 | .input-symbol {
179 |   display: inline-block;
180 |   position: relative;
181 | }
182 | 
183 | .input-symbol.error [class^="icon-"],
184 | .input-symbol.error [class*=" icon-"] {
185 |   color: #ff4400;
186 | }
187 | 
188 | .input-symbol [class^="icon-"],
189 | .input-symbol [class*=" icon-"] {
190 |   left: 1em;
191 | }
192 | 
193 | .input-symbol input {
194 |   padding-left: 3em;
195 | }
196 | 
197 | .input-symbol input {
198 |   width: 100%;
199 | }
200 | 
201 | .input-symbol input:focus + [class^="icon-"],
202 | .input-symbol input:focus + [class*=" icon-"] {
203 |   color: #2cc5d2;
204 | }
205 | 
206 | .input-symbol [class^="icon-"],
207 | .input-symbol [class*=" icon-"] {
208 |   transition: all 300ms ease-in;
209 |   transform: translate3d(0, -50%, 0);
210 |   background: transparent;
211 |   color: #aaa;
212 |   font-size: 1em;
213 |   height: 1em;
214 |   position: absolute;
215 |   top: 50%;
216 |   width: 1em;
217 | }
218 | 
219 | @font-face {
220 |   font-family: "percolate";
221 |   src: url("./assets/icon/percolate.eot?-5w3um4");
222 |   src: url("./assets/icon/percolate.eot?#iefix5w3um4")
223 |       format("embedded-opentype"),
224 |     url("./assets/icon/percolate.woff?5w3um4") format("woff"),
225 |     url("./assets/icon/percolate.ttf?5w3um4") format("truetype"),
226 |     url("./assets/icon/percolate.svg?5w3um4") format("svg");
227 |   font-weight: normal;
228 |   font-style: normal;
229 | }
230 | 
231 | [class^="icon-"],
232 | [class*=" icon-"] {
233 |   font-family: "percolate";
234 | 
235 |   font-style: normal;
236 |   font-weight: normal;
237 |   font-variant: normal;
238 |   text-transform: none;
239 |   line-height: 1;
240 | }
241 | 
242 | .icon-star:before {
243 |   content: "\e608";
244 | }
245 | 
246 | .icon-face-sad:before {
247 |   content: "\e60f";
248 | }
249 | 
250 | .icon-check:before {
251 |   content: "\e65e";
252 | }
253 | 
254 | .list-heading {
255 |   letter-spacing: 0.3em;
256 |   text-indent: 0.3em;
257 |   text-transform: uppercase;
258 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
259 |   font-weight: 800;
260 |   font-size: 11px;
261 |   padding-left: 15px;
262 |   line-height: 40px;
263 |   background: #f8f8f8;
264 |   color: #aaa;
265 | }
266 | 
267 | .list-heading .icon-sync {
268 |   opacity: 1;
269 |   animation: spin 2s infinite linear;
270 |   display: inline-block;
271 |   margin-right: 4px;
272 | }
273 | 
274 | .list-item {
275 |   font-size: 14px;
276 |   line-height: 20px;
277 |   display: flex;
278 |   flex-wrap: wrap;
279 |   height: 3rem;
280 |   width: 100%;
281 |   background: white;
282 |   transition: all ease-out 150ms;
283 | }
284 | 
285 | .list-item .title {
286 |   overflow: hidden;
287 |   text-overflow: ellipsis;
288 |   white-space: nowrap;
289 |   flex: 1;
290 | }
291 | 
292 | .list-item input[type="text"] {
293 |   background: transparent;
294 |   width: 100%;
295 | }
296 | 
297 | .list-item input[type="text"]:focus {
298 |   cursor: text;
299 | }
300 | 
301 | .pin-button {
302 |   width: 3rem;
303 |   height: 3rem;
304 |   background: transparent;
305 |   border: none;
306 |   text-align: center;
307 |   transition: all 200ms ease-in;
308 |   color: #eee;
309 |   font-size: 16px;
310 |   line-height: 3rem;
311 |   outline: none;
312 | }
313 | 
314 | .pin-button:hover {
315 |   color: #2cc5d2;
316 | }
317 | .pin-button:focus {
318 |   outline-color: transparent;
319 | }
320 | 
321 | .pin-button:active {
322 |   color: #555;
323 | }
324 | 
325 | .list-item.TASK_PINNED .icon-star {
326 |   color: #2cc5d2;
327 | }
328 | 
329 | .list-item.TASK_ARCHIVED input[type="text"] {
330 |   color: #a0aec0;
331 |   text-decoration: line-through;
332 | }
333 | 
334 | .list-item:hover {
335 |   background-image: linear-gradient(to bottom, #e5f9f7 0%, #f0fffd 100%);
336 | }
337 | 
338 | .list-item:hover .checkbox {
339 |   cursor: pointer;
340 | }
341 | 
342 | .list-item + .list-item {
343 |   border-top: 1px solid #f0f9fb;
344 | }
345 | 
346 | .list-item.checked input[type="text"] {
347 |   color: #ccc;
348 |   text-decoration: line-through;
349 | }
350 | 
351 | .list-item.checked .delete-item {
352 |   display: inline-block;
353 | }
354 | 
355 | .loading-item {
356 |   height: 3rem;
357 |   width: 100%;
358 |   background: white;
359 |   display: flex;
360 |   align-items: center;
361 |   line-height: 1rem;
362 |   padding-left: 16px;
363 | }
364 | 
365 | .loading-item .glow-checkbox,
366 | .loading-item .glow-text span {
367 |   animation: glow 1.5s ease-in-out infinite;
368 |   background: #eee;
369 |   color: transparent;
370 |   cursor: progress;
371 |   display: inline-block;
372 | }
373 | 
374 | .loading-item .glow-checkbox {
375 |   margin-right: 16px;
376 |   width: 12px;
377 |   height: 12px;
378 | }
379 | 
380 | .loading-item + .loading-item {
381 |   border-top: 1px solid #f0f9fb;
382 | }
383 | 
384 | .list-items {
385 |   position: relative;
386 |   background: white;
387 |   min-height: 288px;
388 | }
389 | 
390 | .list-items .select-placeholder {
391 |   border: none;
392 |   width: 48px;
393 | }
394 | 
395 | .wrapper-message {
396 |   position: absolute;
397 |   top: 45%;
398 |   right: 0;
399 |   bottom: auto;
400 |   left: 0;
401 |   width: auto;
402 |   height: auto;
403 |   transform: translate3d(0, -50%, 0);
404 |   text-align: center;
405 | }
406 | 
407 | .wrapper-message [class^="icon-"],
408 | .wrapper-message [class*=" icon-"] {
409 |   font-size: 48px;
410 |   line-height: 56px;
411 |   color: #2cc5d2;
412 |   display: block;
413 | }
414 | 
415 | .wrapper-message .title-message {
416 |   font-size: 16px;
417 |   line-height: 24px;
418 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
419 |   font-weight: 800;
420 |   color: #4a5568;
421 | }
422 | 
423 | .wrapper-message .subtitle-message {
424 |   font-size: 14px;
425 |   line-height: 20px;
426 |   color: #4a5568;
427 | }
428 | 
429 | .page.lists-show {
430 |   min-height: 100vh;
431 |   background: white;
432 | }
433 | 
434 | .page.lists-show nav {
435 |   background: #d3edf4;
436 |   padding: 1.5rem 1.25rem;
437 |   text-align: center;
438 | }
439 | 
440 | @media screen and (min-width: 40em) {
441 |   .page.lists-show nav {
442 |     text-align: left;
443 |   }
444 | }
445 | 
446 | .page.lists-show nav .title-page {
447 |   font-size: 20px;
448 |   line-height: 24px;
449 |   line-height: 2rem;
450 |   cursor: pointer;
451 |   white-space: nowrap;
452 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
453 |   overflow: hidden;
454 |   text-overflow: ellipsis;
455 |   font-weight: 800;
456 |   color: #1c3f53;
457 |   display: inline-block;
458 |   vertical-align: top;
459 |   max-width: 100%;
460 | }
```

src/main.tsx
```
1 | import { StrictMode } from "react";
2 | import { createRoot } from "react-dom/client";
3 | import App from "./App.tsx";
4 | import "./index.css";
5 | 
6 | createRoot(document.getElementById("root")!).render(
7 |   <StrictMode>
8 |     <App />
9 |   </StrictMode>
10 | );
```

src/types.ts
```
1 | export type TaskData = {
2 |   id: string;
3 |   title: string;
4 |   state: "TASK_ARCHIVED" | "TASK_INBOX" | "TASK_PINNED";
5 | };
```

src/vite-env.d.ts
```
1 | /// <reference types="vite/client" />
```

src/components/InboxScreen.stories.tsx
```
1 | // path: src/components/InboxScreen.stories.tsx
2 | import type { Meta, StoryObj } from "@storybook/react-vite";
3 | 
4 | import { waitFor, waitForElementToBeRemoved } from "storybook/test";
5 | 
6 | import { http, HttpResponse } from "msw";
7 | 
8 | import { MockedState } from "./TaskList.stories";
9 | 
10 | import { Provider } from "react-redux";
11 | 
12 | import InboxScreen from "./InboxScreen";
13 | 
14 | import store from "../lib/store";
15 | 
16 | const meta = {
17 |   component: InboxScreen,
18 |   title: "InboxScreen",
19 |   decorators: [(story) => <Provider store={store}>{story()}</Provider>],
20 |   tags: ["autodocs"],
21 | } satisfies Meta<typeof InboxScreen>;
22 | 
23 | export default meta;
24 | type Story = StoryObj<typeof meta>;
25 | 
26 | export const Default: Story = {
27 |   parameters: {
28 |     msw: {
29 |       handlers: [
30 |         http.get("https://jsonplaceholder.typicode.com/todos?userId=1", () => {
31 |           return HttpResponse.json(MockedState.tasks);
32 |         }),
33 |       ],
34 |     },
35 |   },
36 |   play: async ({ canvas, userEvent }) => {
37 |     // Waits for the component to transition from the loading state
38 |     await waitForElementToBeRemoved(await canvas.findByTestId("loading"));
39 |     // Waits for the component to be updated based on the store
40 |     await waitFor(async () => {
41 |       // Simulates pinning the first task
42 |       await userEvent.click(canvas.getByLabelText("pinTask-1"));
43 |       // Simulates pinning the third task
44 |       await userEvent.click(canvas.getByLabelText("pinTask-3"));
45 |     });
46 |   },
47 | };
48 | 
49 | export const Error: Story = {
50 |   parameters: {
51 |     msw: {
52 |       handlers: [
53 |         http.get("https://jsonplaceholder.typicode.com/todos?userId=1", () => {
54 |           return new HttpResponse(null, {
55 |             status: 403,
56 |           });
57 |         }),
58 |       ],
59 |     },
60 |   },
61 | };
```

src/components/InboxScreen.tsx
```
1 | // path: src/components/InboxScreen.tsx
2 | import { useEffect } from "react";
3 | 
4 | import { useDispatch, useSelector } from "react-redux";
5 | 
6 | import { AppDispatch, fetchTasks, RootState } from "../lib/store";
7 | 
8 | import TaskList from "./TaskList";
9 | 
10 | export default function InboxScreen() {
11 |   const dispatch = useDispatch<AppDispatch>();
12 |   // We're retrieving the error field from our updated store
13 |   const { error } = useSelector((state: RootState) => state.taskbox);
14 |   // The useEffect triggers the data fetching when the component is mounted
15 |   useEffect(() => {
16 |     dispatch(fetchTasks());
17 |   }, [dispatch]);
18 | 
19 |   if (error) {
20 |     return (
21 |       <div className="page lists-show">
22 |         <div className="wrapper-message">
23 |           <span className="icon-face-sad" />
24 |           <p className="title-message">Oh no!</p>
25 |           <p className="subtitle-message">Something went wrong</p>
26 |         </div>
27 |       </div>
28 |     );
29 |   }
30 |   return (
31 |     <div className="page lists-show">
32 |       <nav>
33 |         <h1 className="title-page">Taskbox</h1>
34 |       </nav>
35 |       <TaskList />
36 |     </div>
37 |   );
38 | }
```

src/components/Task.stories.tsx
```
1 | import type { Meta, StoryObj } from "@storybook/react-vite";
2 | 
3 | import { fn } from "storybook/test";
4 | 
5 | import Task from "./Task";
6 | 
7 | export const ActionsData = {
8 |   onArchiveTask: fn(),
9 |   onPinTask: fn(),
10 | };
11 | 
12 | const meta = {
13 |   component: Task,
14 |   title: "Task",
15 |   tags: ["autodocs"],
16 |   //👇 Our exports that end in "Data" are not stories.
17 |   excludeStories: /.*Data$/,
18 |   args: {
19 |     ...ActionsData,
20 |   },
21 | } satisfies Meta<typeof Task>;
22 | 
23 | export default meta;
24 | type Story = StoryObj<typeof meta>;
25 | 
26 | export const Default: Story = {
27 |   args: {
28 |     task: {
29 |       id: "1",
30 |       title: "Test Task",
31 |       state: "TASK_INBOX",
32 |     },
33 |   },
34 | };
35 | 
36 | export const Pinned: Story = {
37 |   args: {
38 |     task: {
39 |       ...Default.args.task,
40 |       state: "TASK_PINNED",
41 |     },
42 |   },
43 | };
44 | 
45 | export const Archived: Story = {
46 |   args: {
47 |     task: {
48 |       ...Default.args.task,
49 |       state: "TASK_ARCHIVED",
50 |     },
51 |   },
52 | };
```

src/components/Task.tsx
```
1 | import type { TaskData } from "../types";
2 | 
3 | type TaskProps = {
4 |   /** Composition of the task */
5 |   task: TaskData;
6 |   /** Event to change the task to archived */
7 |   onArchiveTask: (id: string) => void;
8 |   /** Event to change the task to pinned */
9 |   onPinTask: (id: string) => void;
10 | };
11 | 
12 | export default function Task({
13 |   task: { id, title, state },
14 |   onArchiveTask,
15 |   onPinTask,
16 | }: TaskProps) {
17 |   return (
18 |     <div className={`list-item ${state}`}>
19 |       <label
20 |         htmlFor={`archiveTask-${id}`}
21 |         aria-label={`archiveTask-${id}`}
22 |         className="checkbox"
23 |       >
24 |         <input
25 |           type="checkbox"
26 |           disabled={true}
27 |           name="checked"
28 |           id={`archiveTask-${id}`}
29 |           checked={state === "TASK_ARCHIVED"}
30 |         />
31 |         <span className="checkbox-custom" onClick={() => onArchiveTask(id)} />
32 |       </label>
33 | 
34 |       <label htmlFor={`title-${id}`} aria-label={title} className="title">
35 |         <input
36 |           type="text"
37 |           value={title}
38 |           readOnly={true}
39 |           name="title"
40 |           id={`title-${id}`}
41 |           placeholder="Input title"
42 |         />
43 |       </label>
44 |       {state !== "TASK_ARCHIVED" && (
45 |         <button
46 |           className="pin-button"
47 |           onClick={() => onPinTask(id)}
48 |           id={`pinTask-${id}`}
49 |           aria-label={`pinTask-${id}`}
50 |           key={`pinTask-${id}`}
51 |         >
52 |           <span className={`icon-star`} />
53 |         </button>
54 |       )}
55 |     </div>
56 |   );
57 | }
```

src/components/TaskList.stories.tsx
```
1 | import type { Meta, StoryObj } from "@storybook/react-vite";
2 | 
3 | import type { TaskData } from "../types";
4 | 
5 | import { Provider } from "react-redux";
6 | 
7 | import { configureStore, createSlice } from "@reduxjs/toolkit";
8 | 
9 | import TaskList from "./TaskList";
10 | 
11 | import * as TaskStories from "./Task.stories";
12 | 
13 | // A super-simple mock of the state of the store
14 | export const MockedState = {
15 |   tasks: [
16 |     { ...TaskStories.Default.args.task, id: "1", title: "Task 1" },
17 |     { ...TaskStories.Default.args.task, id: "2", title: "Task 2" },
18 |     { ...TaskStories.Default.args.task, id: "3", title: "Task 3" },
19 |     { ...TaskStories.Default.args.task, id: "4", title: "Task 4" },
20 |     { ...TaskStories.Default.args.task, id: "5", title: "Task 5" },
21 |     { ...TaskStories.Default.args.task, id: "6", title: "Task 6" },
22 |   ] as TaskData[],
23 |   status: "idle",
24 |   error: null,
25 | };
26 | 
27 | // A super-simple mock of a redux store
28 | const Mockstore = ({
29 |   taskboxState,
30 |   children,
31 | }: {
32 |   taskboxState: typeof MockedState;
33 |   children: React.ReactNode;
34 | }) => (
35 |   <Provider
36 |     store={configureStore({
37 |       reducer: {
38 |         taskbox: createSlice({
39 |           name: "taskbox",
40 |           initialState: taskboxState,
41 |           reducers: {
42 |             updateTaskState: (state, action) => {
43 |               const { id, newTaskState } = action.payload;
44 |               const task = state.tasks.findIndex((task) => task.id === id);
45 |               if (task >= 0) {
46 |                 state.tasks[task].state = newTaskState;
47 |               }
48 |             },
49 |           },
50 |         }).reducer,
51 |       },
52 |     })}
53 |   >
54 |     {children}
55 |   </Provider>
56 | );
57 | 
58 | const meta = {
59 |   component: TaskList,
60 |   title: "TaskList",
61 |   decorators: [(story) => <div style={{ margin: "3rem" }}>{story()}</div>],
62 |   tags: ["autodocs"],
63 |   excludeStories: /.*MockedState$/,
64 | } satisfies Meta<typeof TaskList>;
65 | 
66 | export default meta;
67 | type Story = StoryObj<typeof meta>;
68 | 
69 | export const Default: Story = {
70 |   decorators: [
71 |     (story) => <Mockstore taskboxState={MockedState}>{story()}</Mockstore>,
72 |   ],
73 | };
74 | 
75 | export const WithPinnedTasks: Story = {
76 |   decorators: [
77 |     (story) => {
78 |       const pinnedtasks: TaskData[] = [
79 |         ...MockedState.tasks.slice(0, 5),
80 |         { id: "6", title: "Task 6 (pinned)", state: "TASK_PINNED" },
81 |       ];
82 | 
83 |       return (
84 |         <Mockstore
85 |           taskboxState={{
86 |             ...MockedState,
87 |             tasks: pinnedtasks,
88 |           }}
89 |         >
90 |           {story()}
91 |         </Mockstore>
92 |       );
93 |     },
94 |   ],
95 | };
96 | 
97 | export const Loading: Story = {
98 |   decorators: [
99 |     (story) => (
100 |       <Mockstore
101 |         taskboxState={{
102 |           ...MockedState,
103 |           status: "loading",
104 |         }}
105 |       >
106 |         {story()}
107 |       </Mockstore>
108 |     ),
109 |   ],
110 | };
111 | 
112 | export const Empty: Story = {
113 |   decorators: [
114 |     (story) => (
115 |       <Mockstore
116 |         taskboxState={{
117 |           ...MockedState,
118 |           tasks: [],
119 |         }}
120 |       >
121 |         {story()}
122 |       </Mockstore>
123 |     ),
124 |   ],
125 | };
```

src/components/TaskList.tsx
```
1 | import Task from "./Task";
2 | 
3 | import { useDispatch, useSelector } from "react-redux";
4 | 
5 | import { updateTaskState, RootState, AppDispatch } from "../lib/store";
6 | 
7 | export default function TaskList() {
8 |   // We're retrieving our state from the store
9 |   const tasks = useSelector((state: RootState) => {
10 |     const tasksInOrder = [
11 |       ...state.taskbox.tasks.filter((t) => t.state === "TASK_PINNED"),
12 |       ...state.taskbox.tasks.filter((t) => t.state !== "TASK_PINNED"),
13 |     ];
14 |     const filteredTasks = tasksInOrder.filter(
15 |       (t) => t.state === "TASK_INBOX" || t.state === "TASK_PINNED"
16 |     );
17 |     return filteredTasks;
18 |   });
19 |   const { status } = useSelector((state: RootState) => state.taskbox);
20 |   const dispatch = useDispatch<AppDispatch>();
21 |   const pinTask = (value: string) => {
22 |     // We're dispatching the Pinned event back to our store
23 |     dispatch(updateTaskState({ id: value, newTaskState: "TASK_PINNED" }));
24 |   };
25 |   const archiveTask = (value: string) => {
26 |     // We're dispatching the Archive event back to our store
27 |     dispatch(updateTaskState({ id: value, newTaskState: "TASK_ARCHIVED" }));
28 |   };
29 |   const LoadingRow = (
30 |     <div className="loading-item">
31 |       <span className="glow-checkbox" />
32 |       <span className="glow-text">
33 |         <span>Loading</span> <span>cool</span> <span>state</span>
34 |       </span>
35 |     </div>
36 |   );
37 |   if (status === "loading") {
38 |     return (
39 |       <div className="list-items" data-testid="loading" key="loading">
40 |         {LoadingRow}
41 |         {LoadingRow}
42 |         {LoadingRow}
43 |         {LoadingRow}
44 |         {LoadingRow}
45 |         {LoadingRow}
46 |       </div>
47 |     );
48 |   }
49 |   if (tasks.length === 0) {
50 |     return (
51 |       <div className="list-items" key="empty" data-testid="empty">
52 |         <div className="wrapper-message">
53 |           <span className="icon-check" />
54 |           <p className="title-message">You have no tasks</p>
55 |           <p className="subtitle-message">Sit back and relax</p>
56 |         </div>
57 |       </div>
58 |     );
59 |   }
60 | 
61 |   return (
62 |     <div className="list-items" data-testid="success" key="success">
63 |       {tasks.map((task) => (
64 |         <Task
65 |           key={task.id}
66 |           task={task}
67 |           onPinTask={pinTask}
68 |           onArchiveTask={archiveTask}
69 |         />
70 |       ))}
71 |     </div>
72 |   );
73 | }
```

src/lib/store.ts
```
1 | /* A simple redux store/actions/reducer implementation.
2 |  * A true app would be more complex and separated into different files.
3 |  */
4 | import type { TaskData } from "../types";
5 | 
6 | import {
7 |   configureStore,
8 |   createSlice,
9 |   createAsyncThunk,
10 |   PayloadAction,
11 | } from "@reduxjs/toolkit";
12 | 
13 | interface TaskBoxState {
14 |   tasks: TaskData[];
15 |   status: "idle" | "loading" | "failed" | "succeeded";
16 |   error: string | null;
17 | }
18 | 
19 | /*
20 |  * The initial state of our store when the app loads.
21 |  * Usually, you would fetch this from a server. Let's not worry about that now
22 |  */
23 | const TaskBoxData: TaskBoxState = {
24 |   tasks: [],
25 |   status: "idle",
26 |   error: null,
27 | };
28 | /*
29 |  * Creates an asyncThunk to fetch tasks from a remote endpoint.
30 |  * You can read more about Redux Toolkit's thunks in the docs:
31 |  * https://redux-toolkit.js.org/api/createAsyncThunk
32 |  */
33 | export const fetchTasks = createAsyncThunk("taskbox/fetchTasks", async () => {
34 |   const response = await fetch(
35 |     "https://jsonplaceholder.typicode.com/todos?userId=1"
36 |   );
37 |   const data = await response.json();
38 |   const result = data.map(
39 |     (task: { id: number; title: string; completed: boolean }) => ({
40 |       id: `${task.id}`,
41 |       title: task.title,
42 |       state: task.completed ? "TASK_ARCHIVED" : "TASK_INBOX",
43 |     })
44 |   );
45 |   return result;
46 | });
47 | 
48 | /*
49 |  * The store is created here.
50 |  * You can read more about Redux Toolkit's slices in the docs:
51 |  * https://redux-toolkit.js.org/api/createSlice
52 |  */
53 | const TasksSlice = createSlice({
54 |   name: "taskbox",
55 |   initialState: TaskBoxData,
56 |   reducers: {
57 |     updateTaskState: (
58 |       state,
59 |       action: PayloadAction<{ id: string; newTaskState: TaskData["state"] }>
60 |     ) => {
61 |       const task = state.tasks.find((task) => task.id === action.payload.id);
62 |       if (task) {
63 |         task.state = action.payload.newTaskState;
64 |       }
65 |     },
66 |   },
67 |   /*
68 |    * Extends the reducer for the async actions
69 |    * You can read more about it at https://redux-toolkit.js.org/api/createAsyncThunk
70 |    */
71 |   extraReducers(builder) {
72 |     builder
73 |       .addCase(fetchTasks.pending, (state) => {
74 |         state.status = "loading";
75 |         state.error = null;
76 |         state.tasks = [];
77 |       })
78 |       .addCase(fetchTasks.fulfilled, (state, action) => {
79 |         state.status = "succeeded";
80 |         state.error = null;
81 |         // Add any fetched tasks to the array
82 |         state.tasks = action.payload;
83 |       })
84 |       .addCase(fetchTasks.rejected, (state) => {
85 |         state.status = "failed";
86 |         state.error = "Something went wrong";
87 |         state.tasks = [];
88 |       });
89 |   },
90 | });
91 | 
92 | // The actions contained in the slice are exported for usage in our components
93 | export const { updateTaskState } = TasksSlice.actions;
94 | 
95 | /*
96 |  * Our app's store configuration goes here.
97 |  * Read more about Redux's configureStore in the docs:
98 |  * https://redux-toolkit.js.org/api/configureStore
99 |  */
100 | const store = configureStore({
101 |   reducer: {
102 |     taskbox: TasksSlice.reducer,
103 |   },
104 | });
105 | 
106 | // Define RootState and AppDispatch types
107 | export type RootState = ReturnType<typeof store.getState>;
108 | export type AppDispatch = typeof store.dispatch;
109 | 
110 | export default store;
```

src/stories/Button.stories.ts
```
1 | import type { Meta, StoryObj } from "@storybook/react-vite";
2 | import { fn } from "storybook/test";
3 | 
4 | import { Button } from "./Button";
5 | 
6 | // More on how to set up stories at: https://storybook.js.org/docs/writing-stories#default-export
7 | const meta = {
8 |   title: "Example/Button",
9 |   component: Button,
10 |   parameters: {
11 |     // Optional parameter to center the component in the Canvas. More info: https://storybook.js.org/docs/configure/story-layout
12 |     layout: "centered",
13 |   },
14 |   // This component will have an automatically generated Autodocs entry: https://storybook.js.org/docs/writing-docs/autodocs
15 |   tags: ["autodocs"],
16 |   // More on argTypes: https://storybook.js.org/docs/api/argtypes
17 |   argTypes: {
18 |     backgroundColor: { control: "color" },
19 |   },
20 |   // Use `fn` to spy on the onClick arg, which will appear in the actions panel once invoked: https://storybook.js.org/docs/essentials/actions#action-args
21 |   args: { onClick: fn() },
22 | } satisfies Meta<typeof Button>;
23 | 
24 | export default meta;
25 | type Story = StoryObj<typeof meta>;
26 | 
27 | // More on writing stories with args: https://storybook.js.org/docs/writing-stories/args
28 | export const Primary: Story = {
29 |   args: {
30 |     primary: true,
31 |     label: "Button",
32 |   },
33 | };
34 | 
35 | export const Secondary: Story = {
36 |   args: {
37 |     label: "Button",
38 |   },
39 | };
40 | 
41 | export const Large: Story = {
42 |   args: {
43 |     size: "large",
44 |     label: "Button",
45 |   },
46 | };
47 | 
48 | export const Small: Story = {
49 |   args: {
50 |     size: "small",
51 |     label: "Button",
52 |   },
53 | };
```

src/stories/Button.tsx
```
1 | import "./button.css";
2 | 
3 | export interface ButtonProps {
4 |   /** Is this the principal call to action on the page? */
5 |   primary?: boolean;
6 |   /** What background color to use */
7 |   backgroundColor?: string;
8 |   /** How large should the button be? */
9 |   size?: "small" | "medium" | "large";
10 |   /** Button contents */
11 |   label: string;
12 |   /** Optional click handler */
13 |   onClick?: () => void;
14 | }
15 | 
16 | /** Primary UI component for user interaction */
17 | export const Button = ({
18 |   primary = false,
19 |   size = "medium",
20 |   backgroundColor,
21 |   label,
22 |   ...props
23 | }: ButtonProps) => {
24 |   const mode = primary
25 |     ? "storybook-button--primary"
26 |     : "storybook-button--secondary";
27 |   return (
28 |     <button
29 |       type="button"
30 |       className={["storybook-button", `storybook-button--${size}`, mode].join(
31 |         " "
32 |       )}
33 |       style={{ backgroundColor }}
34 |       {...props}
35 |     >
36 |       {label}
37 |     </button>
38 |   );
39 | };
```

src/stories/Configure.mdx
```
1 | import { Meta } from "@storybook/addon-docs/blocks";
2 | 
3 | import Github from "./assets/github.svg";
4 | import Discord from "./assets/discord.svg";
5 | import Youtube from "./assets/youtube.svg";
6 | import Tutorials from "./assets/tutorials.svg";
7 | import Styling from "./assets/styling.png";
8 | import Context from "./assets/context.png";
9 | import Assets from "./assets/assets.png";
10 | import Docs from "./assets/docs.png";
11 | import Share from "./assets/share.png";
12 | import FigmaPlugin from "./assets/figma-plugin.png";
13 | import Testing from "./assets/testing.png";
14 | import Accessibility from "./assets/accessibility.png";
15 | import Theming from "./assets/theming.png";
16 | import AddonLibrary from "./assets/addon-library.png";
17 | 
18 | export const RightArrow = () => <svg 
19 |     viewBox="0 0 14 14" 
20 |     width="8px" 
21 |     height="14px" 
22 |     style={{ 
23 |       marginLeft: '4px',
24 |       display: 'inline-block',
25 |       shapeRendering: 'inherit',
26 |       verticalAlign: 'middle',
27 |       fill: 'currentColor',
28 |       'path fill': 'currentColor'
29 |     }}
30 | >
31 |   <path d="m11.1 7.35-5.5 5.5a.5.5 0 0 1-.7-.7L10.04 7 4.9 1.85a.5.5 0 1 1 .7-.7l5.5 5.5c.2.2.2.5 0 .7Z" />
32 | </svg>
33 | 
34 | <Meta title="Configure your project" />
35 | 
36 | <div className="sb-container">
37 |   <div className='sb-section-title'>
38 |     # Configure your project
39 | 
40 |     Because Storybook works separately from your app, you'll need to configure it for your specific stack and setup. Below, explore guides for configuring Storybook with popular frameworks and tools. If you get stuck, learn how you can ask for help from our community.
41 |   </div>
42 |   <div className="sb-section">
43 |     <div className="sb-section-item">
44 |       <img
45 |         src={Styling}
46 |         alt="A wall of logos representing different styling technologies"
47 |       />
48 |       <h4 className="sb-section-item-heading">Add styling and CSS</h4>
49 |       <p className="sb-section-item-paragraph">Like with web applications, there are many ways to include CSS within Storybook. Learn more about setting up styling within Storybook.</p>
50 |       <a
51 |         href="https://storybook.js.org/docs/react/configure/styling-and-css"
52 |         target="_blank"
53 |       >Learn more<RightArrow /></a>
54 |     </div>
55 |     <div className="sb-section-item">
56 |       <img
57 |         src={Context}
58 |         alt="An abstraction representing the composition of data for a component"
59 |       />
60 |       <h4 className="sb-section-item-heading">Provide context and mocking</h4>
61 |       <p className="sb-section-item-paragraph">Often when a story doesn't render, it's because your component is expecting a specific environment or context (like a theme provider) to be available.</p>
62 |       <a
63 |         href="https://storybook.js.org/docs/react/writing-stories/decorators#context-for-mocking"
64 |         target="_blank"
65 |       >Learn more<RightArrow /></a>
66 |     </div>
67 |     <div className="sb-section-item">
68 |       <img src={Assets} alt="A representation of typography and image assets" />
69 |       <div>
70 |         <h4 className="sb-section-item-heading">Load assets and resources</h4>
71 |         <p className="sb-section-item-paragraph">To link static files (like fonts) to your projects and stories, use the
72 |         `staticDirs` configuration option to specify folders to load when
73 |         starting Storybook.</p>
74 |         <a
75 |           href="https://storybook.js.org/docs/react/configure/images-and-assets"
76 |           target="_blank"
77 |         >Learn more<RightArrow /></a>
78 |       </div>
79 |     </div>
80 |   </div>
81 | </div>
82 | <div className="sb-container">
83 |   <div className='sb-section-title'>
84 |     # Do more with Storybook
85 | 
86 |     Now that you know the basics, let's explore other parts of Storybook that will improve your experience. This list is just to get you started. You can customise Storybook in many ways to fit your needs.
87 |   </div>
88 | 
89 |   <div className="sb-section">
90 |     <div className="sb-features-grid">
91 |       <div className="sb-grid-item">
92 |         <img src={Docs} alt="A screenshot showing the autodocs tag being set, pointing a docs page being generated" />
93 |         <h4 className="sb-section-item-heading">Autodocs</h4>
94 |         <p className="sb-section-item-paragraph">Auto-generate living,
95 |           interactive reference documentation from your components and stories.</p>
96 |         <a
97 |           href="https://storybook.js.org/docs/react/writing-docs/autodocs"
98 |           target="_blank"
99 |         >Learn more<RightArrow /></a>
100 |       </div>
101 |       <div className="sb-grid-item">
102 |         <img src={Share} alt="A browser window showing a Storybook being published to a chromatic.com URL" />
103 |         <h4 className="sb-section-item-heading">Publish to Chromatic</h4>
104 |         <p className="sb-section-item-paragraph">Publish your Storybook to review and collaborate with your entire team.</p>
105 |         <a
106 |           href="https://storybook.js.org/docs/react/sharing/publish-storybook#publish-storybook-with-chromatic"
107 |           target="_blank"
108 |         >Learn more<RightArrow /></a>
109 |       </div>
110 |       <div className="sb-grid-item">
111 |         <img src={FigmaPlugin} alt="Windows showing the Storybook plugin in Figma" />
112 |         <h4 className="sb-section-item-heading">Figma Plugin</h4>
113 |         <p className="sb-section-item-paragraph">Embed your stories into Figma to cross-reference the design and live
114 |           implementation in one place.</p>
115 |         <a
116 |           href="https://storybook.js.org/docs/react/sharing/design-integrations#embed-storybook-in-figma-with-the-plugin"
117 |           target="_blank"
118 |         >Learn more<RightArrow /></a>
119 |       </div>
120 |       <div className="sb-grid-item">
121 |         <img src={Testing} alt="Screenshot of tests passing and failing" />
122 |         <h4 className="sb-section-item-heading">Testing</h4>
123 |         <p className="sb-section-item-paragraph">Use stories to test a component in all its variations, no matter how
124 |           complex.</p>
125 |         <a
126 |           href="https://storybook.js.org/docs/react/writing-tests"
127 |           target="_blank"
128 |         >Learn more<RightArrow /></a>
129 |       </div>
130 |       <div className="sb-grid-item">
131 |         <img src={Accessibility} alt="Screenshot of accessibility tests passing and failing" />
132 |         <h4 className="sb-section-item-heading">Accessibility</h4>
133 |         <p className="sb-section-item-paragraph">Automatically test your components for a11y issues as you develop.</p>
134 |         <a
135 |           href="https://storybook.js.org/docs/react/writing-tests/accessibility-testing"
136 |           target="_blank"
137 |         >Learn more<RightArrow /></a>
138 |       </div>
139 |       <div className="sb-grid-item">
140 |         <img src={Theming} alt="Screenshot of Storybook in light and dark mode" />
141 |         <h4 className="sb-section-item-heading">Theming</h4>
142 |         <p className="sb-section-item-paragraph">Theme Storybook's UI to personalize it to your project.</p>
143 |         <a
144 |           href="https://storybook.js.org/docs/react/configure/theming"
145 |           target="_blank"
146 |         >Learn more<RightArrow /></a>
147 |       </div>
148 |     </div>
149 |   </div>
150 | </div>
151 | <div className='sb-addon'>
152 |   <div className='sb-addon-text'>
153 |     <h4>Addons</h4>
154 |     <p className="sb-section-item-paragraph">Integrate your tools with Storybook to connect workflows.</p>
155 |     <a
156 |         href="https://storybook.js.org/integrations/"
157 |         target="_blank"
158 |       >Discover all addons<RightArrow /></a>
159 |   </div>
160 |   <div className='sb-addon-img'>
161 |     <img src={AddonLibrary} alt="Integrate your tools with Storybook to connect workflows." />
162 |   </div>
163 | </div>
164 | 
165 | <div className="sb-section sb-socials">
166 |     <div className="sb-section-item">
167 |       <img src={Github} alt="Github logo" className="sb-explore-image"/>
168 |       Join our contributors building the future of UI development.
169 | 
170 |       <a
171 |         href="https://github.com/storybookjs/storybook"
172 |         target="_blank"
173 |       >Star on GitHub<RightArrow /></a>
174 |     </div>
175 |     <div className="sb-section-item">
176 |       <img src={Discord} alt="Discord logo" className="sb-explore-image"/>
177 |       <div>
178 |         Get support and chat with frontend developers.
179 | 
180 |         <a
181 |           href="https://discord.gg/storybook"
182 |           target="_blank"
183 |         >Join Discord server<RightArrow /></a>
184 |       </div>
185 |     </div>
186 |     <div className="sb-section-item">
187 |       <img src={Youtube} alt="Youtube logo" className="sb-explore-image"/>
188 |       <div>
189 |         Watch tutorials, feature previews and interviews.
190 | 
191 |         <a
192 |           href="https://www.youtube.com/@chromaticui"
193 |           target="_blank"
194 |         >Watch on YouTube<RightArrow /></a>
195 |       </div>
196 |     </div>
197 |     <div className="sb-section-item">
198 |       <img src={Tutorials} alt="A book" className="sb-explore-image"/>
199 |       <p>Follow guided walkthroughs on for key workflows.</p>
200 | 
201 |       <a
202 |           href="https://storybook.js.org/tutorials/"
203 |           target="_blank"
204 |         >Discover tutorials<RightArrow /></a>
205 |     </div>
206 | </div>
207 | 
208 | <style>
209 |   {`
210 |   .sb-container {
211 |     margin-bottom: 48px;
212 |   }
213 | 
214 |   .sb-section {
215 |     width: 100%;
216 |     display: flex;
217 |     flex-direction: row;
218 |     gap: 20px;
219 |   }
220 | 
221 |   img {
222 |     object-fit: cover;
223 |   }
224 | 
225 |   .sb-section-title {
226 |     margin-bottom: 32px;
227 |   }
228 | 
229 |   .sb-section a:not(h1 a, h2 a, h3 a) {
230 |     font-size: 14px;
231 |   }
232 | 
233 |   .sb-section-item, .sb-grid-item {
234 |     flex: 1;
235 |     display: flex;
236 |     flex-direction: column;
237 |   }
238 | 
239 |   .sb-section-item-heading {
240 |     padding-top: 20px !important;
241 |     padding-bottom: 5px !important;
242 |     margin: 0 !important;
243 |   }
244 |   .sb-section-item-paragraph {
245 |     margin: 0;
246 |     padding-bottom: 10px;
247 |   }
248 | 
249 |   .sb-chevron {
250 |     margin-left: 5px;
251 |   }
252 | 
253 |   .sb-features-grid {
254 |     display: grid;
255 |     grid-template-columns: repeat(2, 1fr);
256 |     grid-gap: 32px 20px;
257 |   }
258 | 
259 |   .sb-socials {
260 |     display: grid;
261 |     grid-template-columns: repeat(4, 1fr);
262 |   }
263 | 
264 |   .sb-socials p {
265 |     margin-bottom: 10px;
266 |   }
267 | 
268 |   .sb-explore-image {
269 |     max-height: 32px;
270 |     align-self: flex-start;
271 |   }
272 | 
273 |   .sb-addon {
274 |     width: 100%;
275 |     display: flex;
276 |     align-items: center;
277 |     position: relative;
278 |     background-color: #EEF3F8;
279 |     border-radius: 5px;
280 |     border: 1px solid rgba(0, 0, 0, 0.05);
281 |     background: #EEF3F8;
282 |     height: 180px;
283 |     margin-bottom: 48px;
284 |     overflow: hidden;
285 |   }
286 | 
287 |   .sb-addon-text {
288 |     padding-left: 48px;
289 |     max-width: 240px;
290 |   }
291 | 
292 |   .sb-addon-text h4 {
293 |     padding-top: 0px;
294 |   }
295 | 
296 |   .sb-addon-img {
297 |     position: absolute;
298 |     left: 345px;
299 |     top: 0;
300 |     height: 100%;
301 |     width: 200%;
302 |     overflow: hidden;
303 |   }
304 | 
305 |   .sb-addon-img img {
306 |     width: 650px;
307 |     transform: rotate(-15deg);
308 |     margin-left: 40px;
309 |     margin-top: -72px;
310 |     box-shadow: 0 0 1px rgba(255, 255, 255, 0);
311 |     backface-visibility: hidden;
312 |   }
313 | 
314 |   @media screen and (max-width: 800px) {
315 |     .sb-addon-img {
316 |       left: 300px;
317 |     }
318 |   }
319 | 
320 |   @media screen and (max-width: 600px) {
321 |     .sb-section {
322 |       flex-direction: column;
323 |     }
324 | 
325 |     .sb-features-grid {
326 |       grid-template-columns: repeat(1, 1fr);
327 |     }
328 | 
329 |     .sb-socials {
330 |       grid-template-columns: repeat(2, 1fr);
331 |     }
332 | 
333 |     .sb-addon {
334 |       height: 280px;
335 |       align-items: flex-start;
336 |       padding-top: 32px;
337 |       overflow: hidden;
338 |     }
339 | 
340 |     .sb-addon-text {
341 |       padding-left: 24px;
342 |     }
343 | 
344 |     .sb-addon-img {
345 |       right: 0;
346 |       left: 0;
347 |       top: 130px;
348 |       bottom: 0;
349 |       overflow: hidden;
350 |       height: auto;
351 |       width: 124%;
352 |     }
353 | 
354 |     .sb-addon-img img {
355 |       width: 1200px;
356 |       transform: rotate(-12deg);
357 |       margin-left: 0;
358 |       margin-top: 48px;
359 |       margin-bottom: -40px;
360 |       margin-left: -24px;
361 |     }
362 |   }
363 |   `}
364 | </style>
```

src/stories/Header.stories.ts
```
1 | import type { Meta, StoryObj } from "@storybook/react-vite";
2 | import { fn } from "storybook/test";
3 | 
4 | import { Header } from "./Header";
5 | 
6 | const meta = {
7 |   title: "Example/Header",
8 |   component: Header,
9 |   // This component will have an automatically generated Autodocs entry: https://storybook.js.org/docs/writing-docs/autodocs
10 |   tags: ["autodocs"],
11 |   parameters: {
12 |     // More on how to position stories at: https://storybook.js.org/docs/configure/story-layout
13 |     layout: "fullscreen",
14 |   },
15 |   args: {
16 |     onLogin: fn(),
17 |     onLogout: fn(),
18 |     onCreateAccount: fn(),
19 |   },
20 | } satisfies Meta<typeof Header>;
21 | 
22 | export default meta;
23 | type Story = StoryObj<typeof meta>;
24 | 
25 | export const LoggedIn: Story = {
26 |   args: {
27 |     user: {
28 |       name: "Jane Doe",
29 |     },
30 |   },
31 | };
32 | 
33 | export const LoggedOut: Story = {};
```

src/stories/Header.tsx
```
1 | import React from "react";
2 | 
3 | import { Button } from "./Button";
4 | import "./header.css";
5 | 
6 | type User = {
7 |   name: string;
8 | };
9 | 
10 | export interface HeaderProps {
11 |   user?: User;
12 |   onLogin?: () => void;
13 |   onLogout?: () => void;
14 |   onCreateAccount?: () => void;
15 | }
16 | 
17 | export const Header = ({
18 |   user,
19 |   onLogin,
20 |   onLogout,
21 |   onCreateAccount,
22 | }: HeaderProps) => (
23 |   <header>
24 |     <div className="storybook-header">
25 |       <div>
26 |         <svg
27 |           width="32"
28 |           height="32"
29 |           viewBox="0 0 32 32"
30 |           xmlns="http://www.w3.org/2000/svg"
31 |         >
32 |           <g fill="none" fillRule="evenodd">
33 |             <path
34 |               d="M10 0h12a10 10 0 0110 10v12a10 10 0 01-10 10H10A10 10 0 010 22V10A10 10 0 0110 0z"
35 |               fill="#FFF"
36 |             />
37 |             <path
38 |               d="M5.3 10.6l10.4 6v11.1l-10.4-6v-11zm11.4-6.2l9.7 5.5-9.7 5.6V4.4z"
39 |               fill="#555AB9"
40 |             />
41 |             <path
42 |               d="M27.2 10.6v11.2l-10.5 6V16.5l10.5-6zM15.7 4.4v11L6 10l9.7-5.5z"
43 |               fill="#91BAF8"
44 |             />
45 |           </g>
46 |         </svg>
47 |         <h1>Acme</h1>
48 |       </div>
49 |       <div>
50 |         {user ? (
51 |           <>
52 |             <span className="welcome">
53 |               Welcome, <b>{user.name}</b>!
54 |             </span>
55 |             <Button size="small" onClick={onLogout} label="Log out" />
56 |           </>
57 |         ) : (
58 |           <>
59 |             <Button size="small" onClick={onLogin} label="Log in" />
60 |             <Button
61 |               primary
62 |               size="small"
63 |               onClick={onCreateAccount}
64 |               label="Sign up"
65 |             />
66 |           </>
67 |         )}
68 |       </div>
69 |     </div>
70 |   </header>
71 | );
```

src/stories/Page.stories.ts
```
1 | import type { Meta, StoryObj } from "@storybook/react-vite";
2 | import { expect, userEvent, within } from "storybook/test";
3 | 
4 | import { Page } from "./Page";
5 | 
6 | const meta = {
7 |   title: "Example/Page",
8 |   component: Page,
9 |   parameters: {
10 |     // More on how to position stories at: https://storybook.js.org/docs/configure/story-layout
11 |     layout: "fullscreen",
12 |   },
13 | } satisfies Meta<typeof Page>;
14 | 
15 | export default meta;
16 | type Story = StoryObj<typeof meta>;
17 | 
18 | export const LoggedOut: Story = {};
19 | 
20 | // More on component testing: https://storybook.js.org/docs/writing-tests/component-testing
21 | export const LoggedIn: Story = {
22 |   play: async ({ canvasElement }) => {
23 |     const canvas = within(canvasElement);
24 |     const loginButton = canvas.getByRole("button", { name: /Log in/i });
25 |     await expect(loginButton).toBeInTheDocument();
26 |     await userEvent.click(loginButton);
27 |     await expect(loginButton).not.toBeInTheDocument();
28 | 
29 |     const logoutButton = canvas.getByRole("button", { name: /Log out/i });
30 |     await expect(logoutButton).toBeInTheDocument();
31 |   },
32 | };
```

src/stories/Page.tsx
```
1 | import React from "react";
2 | 
3 | import { Header } from "./Header";
4 | import "./page.css";
5 | 
6 | type User = {
7 |   name: string;
8 | };
9 | 
10 | export const Page: React.FC = () => {
11 |   const [user, setUser] = React.useState<User>();
12 | 
13 |   return (
14 |     <article>
15 |       <Header
16 |         user={user}
17 |         onLogin={() => setUser({ name: "Jane Doe" })}
18 |         onLogout={() => setUser(undefined)}
19 |         onCreateAccount={() => setUser({ name: "Jane Doe" })}
20 |       />
21 | 
22 |       <section className="storybook-page">
23 |         <h2>Pages in Storybook</h2>
24 |         <p>
25 |           We recommend building UIs with a{" "}
26 |           <a
27 |             href="https://componentdriven.org"
28 |             target="_blank"
29 |             rel="noopener noreferrer"
30 |           >
31 |             <strong>component-driven</strong>
32 |           </a>{" "}
33 |           process starting with atomic components and ending with pages.
34 |         </p>
35 |         <p>
36 |           Render pages with mock data. This makes it easy to build and review
37 |           page states without needing to navigate to them in your app. Here are
38 |           some handy patterns for managing page data in Storybook:
39 |         </p>
40 |         <ul>
41 |           <li>
42 |             Use a higher-level connected component. Storybook helps you compose
43 |             such data from the "args" of child component stories
44 |           </li>
45 |           <li>
46 |             Assemble data in the page component from your services. You can mock
47 |             these services out using Storybook.
48 |           </li>
49 |         </ul>
50 |         <p>
51 |           Get a guided tutorial on component-driven development at{" "}
52 |           <a
53 |             href="https://storybook.js.org/tutorials/"
54 |             target="_blank"
55 |             rel="noopener noreferrer"
56 |           >
57 |             Storybook tutorials
58 |           </a>
59 |           . Read more in the{" "}
60 |           <a
61 |             href="https://storybook.js.org/docs"
62 |             target="_blank"
63 |             rel="noopener noreferrer"
64 |           >
65 |             docs
66 |           </a>
67 |           .
68 |         </p>
69 |         <div className="tip-wrapper">
70 |           <span className="tip">Tip</span> Adjust the width of the canvas with
71 |           the{" "}
72 |           <svg
73 |             width="10"
74 |             height="10"
75 |             viewBox="0 0 12 12"
76 |             xmlns="http://www.w3.org/2000/svg"
77 |           >
78 |             <g fill="none" fillRule="evenodd">
79 |               <path
80 |                 d="M1.5 5.2h4.8c.3 0 .5.2.5.4v5.1c-.1.2-.3.3-.4.3H1.4a.5.5 0 01-.5-.4V5.7c0-.3.2-.5.5-.5zm0-2.1h6.9c.3 0 .5.2.5.4v7a.5.5 0 01-1 0V4H1.5a.5.5 0 010-1zm0-2.1h9c.3 0 .5.2.5.4v9.1a.5.5 0 01-1 0V2H1.5a.5.5 0 010-1zm4.3 5.2H2V10h3.8V6.2z"
81 |                 id="a"
82 |                 fill="#999"
83 |               />
84 |             </g>
85 |           </svg>
86 |           Viewports addon in the toolbar
87 |         </div>
88 |       </section>
89 |     </article>
90 |   );
91 | };
```

src/stories/button.css
```
1 | .storybook-button {
2 |   display: inline-block;
3 |   cursor: pointer;
4 |   border: 0;
5 |   border-radius: 3em;
6 |   font-weight: 700;
7 |   line-height: 1;
8 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
9 | }
10 | .storybook-button--primary {
11 |   background-color: #555ab9;
12 |   color: white;
13 | }
14 | .storybook-button--secondary {
15 |   box-shadow: rgba(0, 0, 0, 0.15) 0px 0px 0px 1px inset;
16 |   background-color: transparent;
17 |   color: #333;
18 | }
19 | .storybook-button--small {
20 |   padding: 10px 16px;
21 |   font-size: 12px;
22 | }
23 | .storybook-button--medium {
24 |   padding: 11px 20px;
25 |   font-size: 14px;
26 | }
27 | .storybook-button--large {
28 |   padding: 12px 24px;
29 |   font-size: 16px;
30 | }
```

src/stories/header.css
```
1 | .storybook-header {
2 |   display: flex;
3 |   justify-content: space-between;
4 |   align-items: center;
5 |   border-bottom: 1px solid rgba(0, 0, 0, 0.1);
6 |   padding: 15px 20px;
7 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
8 | }
9 | 
10 | .storybook-header svg {
11 |   display: inline-block;
12 |   vertical-align: top;
13 | }
14 | 
15 | .storybook-header h1 {
16 |   display: inline-block;
17 |   vertical-align: top;
18 |   margin: 6px 0 6px 10px;
19 |   font-weight: 700;
20 |   font-size: 20px;
21 |   line-height: 1;
22 | }
23 | 
24 | .storybook-header button + button {
25 |   margin-left: 10px;
26 | }
27 | 
28 | .storybook-header .welcome {
29 |   margin-right: 10px;
30 |   color: #333;
31 |   font-size: 14px;
32 | }
```

src/stories/page.css
```
1 | .storybook-page {
2 |   margin: 0 auto;
3 |   padding: 48px 20px;
4 |   max-width: 600px;
5 |   color: #333;
6 |   font-size: 14px;
7 |   line-height: 24px;
8 |   font-family: "Nunito Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
9 | }
10 | 
11 | .storybook-page h2 {
12 |   display: inline-block;
13 |   vertical-align: top;
14 |   margin: 0 0 4px;
15 |   font-weight: 700;
16 |   font-size: 32px;
17 |   line-height: 1;
18 | }
19 | 
20 | .storybook-page p {
21 |   margin: 1em 0;
22 | }
23 | 
24 | .storybook-page a {
25 |   color: inherit;
26 | }
27 | 
28 | .storybook-page ul {
29 |   margin: 1em 0;
30 |   padding-left: 30px;
31 | }
32 | 
33 | .storybook-page li {
34 |   margin-bottom: 8px;
35 | }
36 | 
37 | .storybook-page .tip {
38 |   display: inline-block;
39 |   vertical-align: top;
40 |   margin-right: 10px;
41 |   border-radius: 1em;
42 |   background: #e7fdd8;
43 |   padding: 4px 12px;
44 |   color: #357a14;
45 |   font-weight: 700;
46 |   font-size: 11px;
47 |   line-height: 12px;
48 | }
49 | 
50 | .storybook-page .tip-wrapper {
51 |   margin-top: 40px;
52 |   margin-bottom: 40px;
53 |   font-size: 13px;
54 |   line-height: 20px;
55 | }
56 | 
57 | .storybook-page .tip-wrapper svg {
58 |   display: inline-block;
59 |   vertical-align: top;
60 |   margin-top: 3px;
61 |   margin-right: 4px;
62 |   width: 12px;
63 |   height: 12px;
64 | }
65 | 
66 | .storybook-page .tip-wrapper svg path {
67 |   fill: #1ea7fd;
68 | }
```
