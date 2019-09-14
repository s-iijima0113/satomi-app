<template>
<div class="message-list">
  <div class="message-header">
    <div class="message-box-sort-list">
      <div class="buttom-sort-menu" data-toggle="dropdown">
        <div class="dropdown-background" style="display: none;" />
      </div>
      <div class="content-items-center">
        <div class="icon-list-sort-icon" />
        <div class="text">並び替え</div>
      </div>
    </div>
    <ul class="dropdown-menu-sort-menu">
      <li class="item-current" data-current-item="newest" data-sort="1">
        <div class="message-content">
          <span class="text">日付が新しい順</span>
        </div>
      </li>
      <li class="message-content">
        <span class="text">未開封順</span>
      </li>
    </ul>
  <div class="message-list-content">
    <ul class="hidden-area-list-group">
      <li class="list-entrt" data-user-id="0">
        <div class="flex-parent" />
          <div class="main-photo-circle">
            <div class="photo-area">
              <div class="photo-area-inner" />
            </div>
          </div>
          <div class="message-list-info">
            <div class="profile-info-flex">
              <p class="info-text">
                <span>R</span>
                <span>31才</span>
                <span>東京></span>
              </p>
            </div>
            <div class="list-message">
              <p class="message-contents">
                <span class="message-contents">お疲れ様です！</span>
              </p>
            </div>
            <div class="action-area">
              <time>17分前</time>
            </div>
          </div>
          <div class="js-dwordown">
            <div data-toggle="dropdown">
              <div class="js-click-area">
                <span class="icon-option-gray" />
              </div>
              <div class="dropdown-background-backdrop" style="display: none" />
            </div>
          </div>
        <ul class="dropdown-menu-message-action">
          <li class="item">
            <div class="js-message-item-delate">
              <span class="text">削除する</span>
            </div>
          </li>
        </ul>
      </li>
    </ul>
  </div>
  </div>
</div>
</template>
