classDiagram
direction BT
class Attraction {
  - String image
  - double distanceFromMC
  - String contentId
  - String homepage
  - double MULTI_CAMPUS_LONGITUDE
  - double MULTI_CAMPUS_LATITUDE
  - String tel
  - String title
  - String longitude
  - String latitude
  - String overview
  - String addr2
  - String contentTypeId
  - String addr1
}
class AttractionController {
  - Logger logger
  - AttractionService service
}
class AttractionDBUtil
class AttractionDao {
<<Interface>>

}
class AttractionException
class AttractionRestController {
  - AttractionService service
  - String SUCCESS
  - Logger logger
}
class AttractionService {
<<Interface>>

}
class AttractionServiceImp {
  - AttractionDao dao
}
class BookException
class DBUtil
class EnjoyTripSpringbootApplication
class EnjoyTripSpringbootApplicationTests
class FileDownLoadView
class FileDownloadController {
  - Logger logger
  - String uploadPath
}
class FileInfoDto {
  - String fileId
  - String saveFile
  - String saveFolder
  - String originalFile
}
class HomeController {
  - Logger logger
}
class HotPlace {
  - int hotId
  - String userId
  - MultipartFile[] fileup
  - int hit
  - List~FileInfoDto~ fileInfos
  - String title
  - String content
  - String createDate
}
class HotPlaceController {
  - ServletContext servletContext
  - String realPath
  - String key
  - String word
  - long serialVersionUID
  - HotPlaceServiceImpl boardService
  - String queryStrig
  - Logger logger
  - int pgno
}
class HotPlaceDao {
<<Interface>>

}
class HotPlacePageBean {
  - String pageLink
  - String key
  - int interval
  - String word
  - int pageNo
  - String order
  - int start
}
class HotPlaceRestController {
  - String FAIL
  - Logger logger
  - ServletContext servletContext
  - HotPlaceServiceImpl boardService
  - String SUCCESS
}
class HotPlaceService {
<<Interface>>

}
class HotPlaceServiceImpl {
  - HotPlaceDao boardDao
  - String realPath
  - Logger logger
}
class InfoBoard {
  - String createDate
  - String title
  - String content
  - int infoId
  - String userId
  - int hit
}
class InfoBoardController {
  - String queryStrig
  - long serialVersionUID
  - InfoBoardService boardService
  - int pgno
  - String word
  - Logger logger
  - String key
}
class InfoBoardDao {
<<Interface>>

}
class InfoBoardRestController {
  - String SUCCESS
  - String FAIL
  - InfoBoardService boardService
  - Logger logger
}
class InfoBoardService {
<<Interface>>

}
class InfoBoardServiceImpl {
  - Logger logger
  - InfoBoardDao boardDao
}
class JwtService {
<<Interface>>

}
class JwtServiceImpl {
  + Logger logger
  - int REFRESH_TOKEN_EXPIRE_MINUTES
  - String SALT
  - int EXPIRE_MINUTES
  - int ACCESS_TOKEN_EXPIRE_MINUTES
}
class JwtServiceImpl2 {
  - int ACCESS_TOKEN_EXPIRE_MINUTES
  + Logger logger
  - int EXPIRE_MINUTES
  - int REFRESH_TOKEN_EXPIRE_MINUTES
  - String SALT
}
class PageBean {
  - String key
  - String word
  - int start
  - int pageNo
  - String order
  - String pageLink
  - int interval
}
class PageUtility {
  ~ int lastpagecount
  ~ String imagepath
  ~ int beforetenpage
  ~ int displayrowcount
  ~ int pagePercount
  ~ int beforepagecount
  ~ int currentpagecount
  ~ int nexttenpage
  ~ int firstpagecount
  ~ int totalpagecount
  ~ String search
  ~ int totalrowcount
  ~ int nextpagecount
}
class ParameterCheck
class SearchOption {
  ~ String contentTypeId
  ~ String keyword
  ~ String sido
  ~ String gugun
}
class SizeConstant {
  + int LIST_SIZE
  + int NAVIGATION_SIZE
}
class SwaggerConfiguration {
  - String title
  - String version
}
class UnAuthorizedException {
  - long serialVersionUID
}
class User {
  - String nickname
  - String userid
  - String email
  - String name
  - String userpwd
}
class UserController {
  - UserService userService
  + Logger logger
  - String FAIL
  - String SUCCESS
  - JwtServiceImpl jwtService
}
class UserDao {
<<Interface>>

}
class UserException
class UserService {
<<Interface>>

}
class UserServiceImp {
  - UserDao dao
}
class WebMvcConfiguration {
  - List~String~ patterns
  - String uploadPath
}

AttractionServiceImp  ..>  AttractionService 
HotPlaceServiceImpl  ..>  HotPlaceService 
InfoBoardServiceImpl  ..>  InfoBoardService 
JwtServiceImpl  ..>  JwtService 
JwtServiceImpl2  ..>  JwtService 
UserServiceImp  ..>  UserService 
