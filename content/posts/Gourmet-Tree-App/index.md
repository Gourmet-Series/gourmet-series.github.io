---
title: "Gourmet Tree App"
date: 2023-02-08T04:27:26+09:00
draft: false
---


# 고메 트리(Gourmet Tree) 도움말

## 목차
1. [화면 구성](#h1)
2. [문법](#h2)
3. [내보내기](#h3)
4. [연락처](#h4)
5. [외부 라이브러리 및 라이센스](#h5)


<h2 id="h1">1. 화면 구성</h2>
{{ $image := .Resources.GetMatch "img1.png" }}
<img src="{{ $image.RelPermalink }}" width="{{ $image.Width }}" height="{{ $image.Height }}">

- Gourmet Tree는 에디터(좌측)와 미리보기(우측)로 구성되어 있습니다.
- <img class=icon src="icons/slice1.png"> 버튼은 파일을 저장하고, 현재 편집창을 닫습니다.
- <img class=icon src="icons/slice2.png"> 버튼은 도움말을 다시 보여줍니다.
- <img class=icon src="icons/slice3.png"> 버튼은 미리보기 창을 보여줍니다.
- <img class=icon src="icons/slice4.png"> 버튼은 내보내기 메뉴를 보여줍니다. 
- <img class=icon src="icons/slice5.png"> 버튼은 미리보기를 넓게 보여주거나, 좁게 보여줍니다.


<h2 id="h2">2. 문법</h2>
- 하위항목을 지정하기 위해서는 탭을 사용하세요.
- 줄 맨 끝에서 '\\\\'<i>역슬래시 두 개</i> 기호를 사용하여 아래로 내려간 트리를 그리세요.
	- \* 역슬래시는 대체로 엔터 혹은 리턴키(⮐) 위에 있습니다.
- 줄 내에서도 '\\\\' 기호를 사용하여 줄바꿈을 할 수 있습니다.

<table>
	<th>문법</th>
	<th>결과</th>
	<tr>
		<td class=tabbed>

	```
	항목 1
	 ⇥ 항목 1-1
	 ⇥ 항목 1-2
	항목 2
	 ⇥ 항목 3
	 ⇥  ⇥ 항목 4
	```

</td>
	<td class=center><img src="img2.png"></td>
	</tr>
		<tr>
	<td class=tabbed>

```
항목 1 \\
 ⇥ 항목 2 \\
 	 ⇥  ⇥ 항목 2-2
 ⇥ 항목 3
```
</td>
<td class=center><img src="img3.png"></td>
</tr>
		<tr>
	<td class=tabbed>

```
item 1
 ⇥ newline \\ here
```
</td>
<td class=center><img src="img4.png"></td>
</tr>
</table>

- 텍스트를 강조하거나, 밑줄을 긋고 배경색깔을 바꿀 수 있습니다.
- "\*, \_" 기호를 표시하기 위해서는 앞에 "\\" 기호를 붙여서 "\\\*", "\\\_"와 같은 형태로 사용해주세요.

<table class=center>
	<tr>
		<th>항목</th>
		<th>문법</th>
		<th>결과</th>
	</tr>
	<tr>
		<td>강조</td>
		<td>\*굵게\*</td>
		<td><b>굵게</b></td>
	</tr>
	<tr>
		<td>밑줄</td>
		<td>\_밑줄\_</td>
		<td><u>밑줄</u></td>
	</tr>
	<tr>
		<td>취소선</td>
		<td>~취소선~</td>
		<td><strike>취소선</strike></td>
	</tr>
	<tr>
		<td>어두운 배경</td>
		<td>\*\*어두운 배경\*\*</td>
		<td><strong>어두운 배경</strong></td>
	</tr>
	<tr>
		<td>회색 배경</td>
		<td>+\*회색 배경\*+</td>
		<td><strong class=grey>회색 배경</strong></td>
	</tr>
	<tr>
		<td>외곽선</td>
		<td>-\*외곽선\*-</td>
		<td><strong class=outline>외곽선</strong></td>
	</tr>
	<tr>
		<td>여린 글자</td>
		<td>"여린 글자"</td>
		<td><i>여린 글자</i></td>
	</tr>
	<tr>
		<td>주석</td>
		<td># 주석 내용 ..</td>
		<td></td>
	</tr>
</table>

<h2 id="h3">3. 내보내기</h2>
- 그림으로 내보내기, PDF로 내보내기 기능을 각 지원합니다.
- PDF로 내보내기는 단일 페이지로 내보내기, 여러 페이지로 내보내기를 지원합니다.
	- 단일 페이지로 내보내기는 문서를 단일 페이지로 이루어진 PDF로 내보냅니다.
	- 여러 페이지로 내보내기는 트리를 A4 크기의 여러 페이지로 이루어진 PDF로 내보냅니다.
- 그림으로 내보내기
	- PNG 파일로 내보냅니다.
- 문서의 길이가 기기에서 처리 가능한 길이를 넘을 경우, 여러 페이지 PDF 내보내기만 가능합니다.


<h2 id="h4">4. 연락처</h2>
- <a href="mailto:gourmet.series@icloud.com">gourmet.series@icloud.com</a>


<h2 id="h5">5. 외부 라이브러리 및 라이센스</h2>
 <b>Code Editor View</b> Copyright [2021..2022] Manuel M. T. Chakravarty. <a href="https://github.com/mchakravarty/CodeEditorView">[🔗]</a>
 
 <b>작명 도움: MIJI</b>

Distributed under the Apache-2.0 license — see the below for details.

```

                              Apache License
                        Version 2.0, January 2004
                     http://www.apache.org/licenses/

TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

1. Definitions.

   "License" shall mean the terms and conditions for use, reproduction,
   and distribution as defined by Sections 1 through 9 of this document.

   "Licensor" shall mean the copyright owner or entity authorized by
   the copyright owner that is granting the License.

   "Legal Entity" shall mean the union of the acting entity and all
   other entities that control, are controlled by, or are under common
   control with that entity. For the purposes of this definition,
   "control" means (i) the power, direct or indirect, to cause the
   direction or management of such entity, whether by contract or
   otherwise, or (ii) ownership of fifty percent (50%) or more of the
   outstanding shares, or (iii) beneficial ownership of such entity.

   "You" (or "Your") shall mean an individual or Legal Entity
   exercising permissions granted by this License.

   "Source" form shall mean the preferred form for making modifications,
   including but not limited to software source code, documentation
   source, and configuration files.

   "Object" form shall mean any form resulting from mechanical
   transformation or translation of a Source form, including but
   not limited to compiled object code, generated documentation,
   and conversions to other media types.

   "Work" shall mean the work of authorship, whether in Source or
   Object form, made available under the License, as indicated by a
   copyright notice that is included in or attached to the work
   (an example is provided in the Appendix below).

   "Derivative Works" shall mean any work, whether in Source or Object
   form, that is based on (or derived from) the Work and for which the
   editorial revisions, annotations, elaborations, or other modifications
   represent, as a whole, an original work of authorship. For the purposes
   of this License, Derivative Works shall not include works that remain
   separable from, or merely link (or bind by name) to the interfaces of,
   the Work and Derivative Works thereof.

   "Contribution" shall mean any work of authorship, including
   the original version of the Work and any modifications or additions
   to that Work or Derivative Works thereof, that is intentionally
   submitted to Licensor for inclusion in the Work by the copyright owner
   or by an individual or Legal Entity authorized to submit on behalf of
   the copyright owner. For the purposes of this definition, "submitted"
   means any form of electronic, verbal, or written communication sent
   to the Licensor or its representatives, including but not limited to
   communication on electronic mailing lists, source code control systems,
   and issue tracking systems that are managed by, or on behalf of, the
   Licensor for the purpose of discussing and improving the Work, but
   excluding communication that is conspicuously marked or otherwise
   designated in writing by the copyright owner as "Not a Contribution."

   "Contributor" shall mean Licensor and any individual or Legal Entity
   on behalf of whom a Contribution has been received by Licensor and
   subsequently incorporated within the Work.

2. Grant of Copyright License. Subject to the terms and conditions of
   this License, each Contributor hereby grants to You a perpetual,
   worldwide, non-exclusive, no-charge, royalty-free, irrevocable
   copyright license to reproduce, prepare Derivative Works of,
   publicly display, publicly perform, sublicense, and distribute the
   Work and such Derivative Works in Source or Object form.

3. Grant of Patent License. Subject to the terms and conditions of
   this License, each Contributor hereby grants to You a perpetual,
   worldwide, non-exclusive, no-charge, royalty-free, irrevocable
   (except as stated in this section) patent license to make, have made,
   use, offer to sell, sell, import, and otherwise transfer the Work,
   where such license applies only to those patent claims licensable
   by such Contributor that are necessarily infringed by their
   Contribution(s) alone or by combination of their Contribution(s)
   with the Work to which such Contribution(s) was submitted. If You
   institute patent litigation against any entity (including a
   cross-claim or counterclaim in a lawsuit) alleging that the Work
   or a Contribution incorporated within the Work constitutes direct
   or contributory patent infringement, then any patent licenses
   granted to You under this License for that Work shall terminate
   as of the date such litigation is filed.

4. Redistribution. You may reproduce and distribute copies of the
   Work or Derivative Works thereof in any medium, with or without
   modifications, and in Source or Object form, provided that You
   meet the following conditions:

   (a) You must give any other recipients of the Work or
       Derivative Works a copy of this License; and

   (b) You must cause any modified files to carry prominent notices
       stating that You changed the files; and

   (c) You must retain, in the Source form of any Derivative Works
       that You distribute, all copyright, patent, trademark, and
       attribution notices from the Source form of the Work,
       excluding those notices that do not pertain to any part of
       the Derivative Works; and

   (d) If the Work includes a "NOTICE" text file as part of its
       distribution, then any Derivative Works that You distribute must
       include a readable copy of the attribution notices contained
       within such NOTICE file, excluding those notices that do not
       pertain to any part of the Derivative Works, in at least one
       of the following places: within a NOTICE text file distributed
       as part of the Derivative Works; within the Source form or
       documentation, if provided along with the Derivative Works; or,
       within a display generated by the Derivative Works, if and
       wherever such third-party notices normally appear. The contents
       of the NOTICE file are for informational purposes only and
       do not modify the License. You may add Your own attribution
       notices within Derivative Works that You distribute, alongside
       or as an addendum to the NOTICE text from the Work, provided
       that such additional attribution notices cannot be construed
       as modifying the License.

   You may add Your own copyright statement to Your modifications and
   may provide additional or different license terms and conditions
   for use, reproduction, or distribution of Your modifications, or
   for any such Derivative Works as a whole, provided Your use,
   reproduction, and distribution of the Work otherwise complies with
   the conditions stated in this License.

5. Submission of Contributions. Unless You explicitly state otherwise,
   any Contribution intentionally submitted for inclusion in the Work
   by You to the Licensor shall be under the terms and conditions of
   this License, without any additional terms or conditions.
   Notwithstanding the above, nothing herein shall supersede or modify
   the terms of any separate license agreement you may have executed
   with Licensor regarding such Contributions.

6. Trademarks. This License does not grant permission to use the trade
   names, trademarks, service marks, or product names of the Licensor,
   except as required for reasonable and customary use in describing the
   origin of the Work and reproducing the content of the NOTICE file.

7. Disclaimer of Warranty. Unless required by applicable law or
   agreed to in writing, Licensor provides the Work (and each
   Contributor provides its Contributions) on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
   implied, including, without limitation, any warranties or conditions
   of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
   PARTICULAR PURPOSE. You are solely responsible for determining the
   appropriateness of using or redistributing the Work and assume any
   risks associated with Your exercise of permissions under this License.

8. Limitation of Liability. In no event and under no legal theory,
   whether in tort (including negligence), contract, or otherwise,
   unless required by applicable law (such as deliberate and grossly
   negligent acts) or agreed to in writing, shall any Contributor be
   liable to You for damages, including any direct, indirect, special,
   incidental, or consequential damages of any character arising as a
   result of this License or out of the use or inability to use the
   Work (including but not limited to damages for loss of goodwill,
   work stoppage, computer failure or malfunction, or any and all
   other commercial damages or losses), even if such Contributor
   has been advised of the possibility of such damages.

9. Accepting Warranty or Additional Liability. While redistributing
   the Work or Derivative Works thereof, You may choose to offer,
   and charge a fee for, acceptance of support, warranty, indemnity,
   or other liability obligations and/or rights consistent with this
   License. However, in accepting such obligations, You may act only
   on Your own behalf and on Your sole responsibility, not on behalf
   of any other Contributor, and only if You agree to indemnify,
   defend, and hold each Contributor harmless for any liability
   incurred by, or claims asserted against, such Contributor by reason
   of your accepting any such warranty or additional liability.

END OF TERMS AND CONDITIONS

```

