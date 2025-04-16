# -cenjifdgdgdgdfgdfg
<div class="navbar navbar-expand-lg navbar-dark bg-indigo navbar-static">
  <div class="d-flex flex-1 d-lg-none">

    <button class="navbar-toggler sidebar-mobile-main-toggle" type="button" id="toggler">
      <i class="icon-paragraph-justify3"></i>
    </button>
  </div>

  <div class="navbar-brand text-center text-lg-left">
    <a href="javascript:;" class="d-inline-block">
      <img src="assets/images/logo_small_dark.png" alt="">
    </a>
  </div>


  <ul class="navbar-nav flex-row order-1 order-lg-2 flex-1  justify-content-end align-items-center">

    <li class="nav-item" *ngIf="this.getToken('role')=='DOCTR' ||this.getToken('role')=='SUADM'"
      style="margin-top: 6px;">
      <a href="javascript:;" class="navbar-nav-link navbar-nav-link-toggler" (click)="redirectPage('WHATSAPP')">
        <i class="fab fa-whatsapp"></i>
        <span class="badge badge-warning badge-pill ml-auto ml-lg-0"> {{this.getToken('whatsappCount')}}
        </span>
      </a>
    </li>

    <li class="nav-item">
      <a href="javascript:;" class="navbar-nav-link navbar-nav-link-toggler">
        <span class="font-weight-600"> {{'BRANCHES.branch'|translate}} : {{branchList?.branchName?branchList?.branchName:'Madhapur'}} </span>
      </a>fghghgfhg
    </li>

    <li class="">
      <a href="https://api.whatsapp.com/send?phone=+917396022236&amp;text=Hello" *ngIf="this.getToken('role')=='CUSTM'"
        target="_blank">
        <i class="fab fa-whatsapp"></i>
      </a>
    </li>

   <li class="nav-item nav-item-dropdown-lg dropdown dropdown-user h-100">
  <a href="javascript:;" class="navbar-nav-link navbar-nav-link-toggler dropdown-toggle d-inline-flex align-items-center h-100" data-toggle="dropdown">
    <img alt='' style="width: 40px;" class="rounded-pill mr-lg-2" [src]="(this.getToken('profilePic')?this.base64Image+this.getToken('profilePic'):'assets/images/header-profile.png')" /> 
    <div> <span class='username'>{{this.getToken('username')}}  </span></div>
  </a>

  <div class="dropdown-menu dropdown-menu-right">
    <a href="javascript:;" class="dropdown-item" [routerLink]="['/main/my-profile']">
      <i class="icon-user-plus"></i> {{'HEADER.Myprofile'|translate}}
    </a>

    <div class="dropdown-divider"></div>

    <!-- Language dropdown trigger and menu combined -->
    <div class="dropdown-item dropdown-toggle" id="languageDropdown" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
      <i class="icon-earth"></i> {{ 'HEADER.Languages' | translate }}
    </div>
    <div class="dropdown-menu" aria-labelledby="languageDropdown">
      <a href="javascript:;" class="dropdown-item" (click)="setLanguage('en')">{{'HEADER.English'|translate}}</a>
      <a href="javascript:;" class="dropdown-item" (click)="setLanguage('hi')">{{'HEADER.Hindi'|translate}}</a>
      <a href="javascript:;" class="dropdown-item" (click)="setLanguage('te')">{{'HEADER.telugu'|translate}}</a>
      <a href="javascript:;" class="dropdown-item" (click)="setLanguage('ta')">{{'HEADER.tamil'|translate}}</a>
      <a href="javascript:;" class="dropdown-item" (click)="setLanguage('ka')">{{'HEADER.kannada'|translate}}</a>
      <a href="javascript:;" class="dropdown-item" (click)="setLanguage('ml')">{{'HEADER.malayalam'|translate}}</a>
    </div>

    <div class="dropdown-divider"></div>
    <a href="javascript:;" [routerLink]="['/main/change-password']" class="dropdown-item">
      <i class="icon-lock5"></i> {{'HEADER.ChangePassword'|translate}}
    </a>
    <a href="javascript:;" class="dropdown-item" (click)="logout()">
      <i class="icon-switch2"></i> {{'HEADER.Logout'|translate}}
    </a>
  </div>
</li>









cxgdfdfdfdfdfdfdfdfdfdfdfdfdfdfdfdfdfdfdfdfdf



    
    <li class="nav-item">
      <a href="javascript:;" class="navbar-nav-link navbar-nav-link-toggler" (click)="redirectPage('APPL')">
        <i class="fa fa-bell"></i>
        <span class="badge badge-warning badge-pill ml-auto ml-lg-0" *ngIf="this.getToken('notificationCount')>0">
          {{ this.getToken('notificationCount')}}
        </span>
      </a>
    </li>
  </ul>
</div>