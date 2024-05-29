# MUI 설치 방법
```bash
npm install @mui/material @mui/icons-material @emotion/react @emotion/styled
```

# 텍스트 필드 컴포넌트
```jsx
import { TextField } from '@mui/material'

<TextField id="username" label="아이디" type='text' variant='filled' fullWidth={true} margin="none" required />
```

- 속성
  - id: 텍스트 필드 식별자
  - label: 브라우저의 UI에 보여지는 텍스트 필드
  - type: "text", "password", "date", "time"
  - variant (텍스트 필드의 UI 스타일): "outlined", "filled", "standard"
  - fullWidth: 태그가 들어가 있는 컨테이너의 전체 너비를 차지하게 만든다.
  - margin (태그의 위와 아래에 들어가는 여백): "none", "dense", "normal"
  - required
  - disabled
- 참고: https://mui.com/material-ui/react-text-field/

# 체크박스 컴포넌트
```jsx
import { Checkbox, FormControlLabel } from '@mui/material'

<FormControlLabel id='save-id' label="아이디 저장" labelPlacement='top' control={<Checkbox color='primary' />} />
```

- 보통 설명 text를 같이 쓰기 위해 `FormControlLabel` 태그 의 control 속성으로 `Checkbox` 태그를 설정한다.

- Checkbox의 속성
  - color: "primary", "secondary", "default", "success"
- FormControlLabel의 속성
  - label: 체크박스에 대한 설명
  - labelPlacement (설명의 위치): "top", "start", "bottom", "end"


- 참고: https://mui.com/material-ui/react-checkbox/

# 버튼 컴포넌트
```jsx
import { Button } from '@mui/material';

<Button id="send" variant='contained' href='https://www.naver.com' size='large' color='primary' fullWidth sx={{ mt: 2, mb: 2 }}>전송</Button>
```

- 속성
  - variant (브라우저에 보이는 UI 스타일): "text", "contained", "outlined"
  - href: 이동할 링크 주소
  - size (버튼 크기): "small", "medium", "large"
  - color: "success", "secondary"
  - fullWidth: 컨테이너 너비 전체를 차지하게 만든다.
  - sx (Styled System): CSS를 컴포넌트 안에 입력할수 있게 만든다.
  

- 참고: https://mui.com/material-ui/react-button/

# Typography
```jsx
import { Typography } from '@mui/material';

<Typography variant="h1">회원가입</Typography>
```

- MUI에서 텍스트 스타일을 지정 할때 사용한다.
- 속성
  - variant: html 스타일

참고: https://mui.com/material-ui/api/typography/



# Layout
# Container
```jsx
import { Container } from '@mui/material';

<Container maxWidth="xs" fixed sx={{ backgroundColor: "#a00" }} >
  <h1>제목</h1>
</Container>
```

- 페이지 요소를 중앙에 배치하고 양쪽에 여백을 넣기 위해 사용한다.
- 속성
  - maxWidth (최대 너비): xs < sm < md < lg (기본값) < xl
  - fixed: 화면의 크기에 따라 최대 너비가 자동으로 조절된다.


- 참고: https://mui.com/material-ui/react-container/

# Box
```jsx
import { Box } from '@mui/material';

<Box display="flex" flexDirection="column" alignItems="center" >
  <h1>로그인</h1>
</Box>
```

- html에서 `div`와 같은 역할을 한다.
- 속성
  - display: 자유롭게 가로와 세로를 조정 할 수 있는 flex 태그로 감싼다.
  - flexDirection (flex 태그 안에서 배치 방향): row (수평 배치), column (수직 배치)
  - alignItems (정렬 방식): "flex-start" (왼쪽 정렬), "center" (가운데 정렬), "flex-end" (오른쪽 정렬)
- 참고: https://mui.com/material-ui/react-box/

# Grid 컴포넌트
```jsx
import { Grid, Box } from '@mui/material';

<Grid container>
  <Grid item xs={4} sm={12}>
    <Box sx={{ backgroundColor: "#a00" }}>
      <h1>시작</h1>
    </Box>
  </Grid>
  <Grid item xs={4} sm={12}>
    <Box sx={{ backgroundColor: "#3b3" }}>
      <h1>중간</h1>
    </Box>
  </Grid>
  <Grid item xs={4} sm={12}>
    <Box sx={{ backgroundColor: "#08b" }}>
      <h1>끝</h1>
    </Box>
  </Grid>
</Grid>
```


- 속성
  - container: Grid item을 담는 태그이다.
  - item: Grid container 태그 안에 있어야 한다.
  - xs: 브라우저 화면이 0px 이상일때 보여지는 비율
  - sm: 브라우저 화면이 600px 이상일때 보여지는 비율
  - md: 브라우저 화면이 900px 이상일때 보여지는 비율
  - lg: 브라우저 화면이 1200px 이상일때 보여지는 비율
  - xl: 브라우저 화면이 1536px 이상일때 보여지는 비율
- 화면 크기 (xs,sm,md,lg,xl)에 따라 차지하는 공간을 다르게 만든다.
- 최대 너비를 12를 기준으로 화면 크기에 따라 비율을 설정한다.


참고: https://mui.com/material-ui/react-grid/


