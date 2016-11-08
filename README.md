# backend-interview
/*
Navicat MySQL Data Transfer

Source Server         : localhost_3306
Source Server Version : 50129
Source Host           : localhost:3306
Source Database       : test

Target Server Type    : MYSQL
Target Server Version : 50129
File Encoding         : 65001

Date: 2016-11-08 13:10:18
*/

SET FOREIGN_KEY_CHECKS=0;

-- ----------------------------
-- Table structure for `bicuser`
-- ----------------------------
DROP TABLE IF EXISTS `bicuser`;
CREATE TABLE `bicuser` (
  `userid` int(10) NOT NULL AUTO_INCREMENT,
  `weixin` char(16) DEFAULT NULL,
  `email` char(20) DEFAULT NULL,
  `phone` char(14) DEFAULT NULL,
  `summoney` double(7,2) NOT NULL,
  PRIMARY KEY (`userid`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of bicuser
-- ----------------------------
INSERT INTO `bicuser` VALUES ('1', null, '1204012618@qq.com', null, '50.00');
INSERT INTO `bicuser` VALUES ('2', null, null, '15735806945', '0.00');




--------------------------------------------------------------------------------------------------
/*
Navicat MySQL Data Transfer

Source Server         : localhost_3306
Source Server Version : 50129
Source Host           : localhost:3306
Source Database       : test

Target Server Type    : MYSQL
Target Server Version : 50129
File Encoding         : 65001

Date: 2016-11-08 13:10:09
*/

SET FOREIGN_KEY_CHECKS=0;

-- ----------------------------
-- Table structure for `recharge`
-- ----------------------------
DROP TABLE IF EXISTS `recharge`;
CREATE TABLE `recharge` (
  `rechargeid` int(20) NOT NULL,
  `userid` int(10) NOT NULL,
  `recharge` float(7,2) DEFAULT NULL,
  `time` date NOT NULL,
  PRIMARY KEY (`rechargeid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of recharge
-- ----------------------------
INSERT INTO `recharge` VALUES ('1', '1', '50.00', '2016-11-01');




--------------------------------------------------------
/*
Navicat MySQL Data Transfer

Source Server         : localhost_3306
Source Server Version : 50129
Source Host           : localhost:3306
Source Database       : test

Target Server Type    : MYSQL
Target Server Version : 50129
File Encoding         : 65001

Date: 2016-11-08 13:48:49
*/

SET FOREIGN_KEY_CHECKS=0;

-- ----------------------------
-- Table structure for `riding`
-- ----------------------------
DROP TABLE IF EXISTS `riding`;
CREATE TABLE `riding` (
  `ridingid` int(20) NOT NULL AUTO_INCREMENT,
  `userid` int(10) NOT NULL,
  ` begin` varchar(50) NOT NULL,
  `end` varchar(50) DEFAULT NULL,
  `date` date NOT NULL,
  PRIMARY KEY (`ridingid`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of riding
-- ----------------------------
INSERT INTO `riding` VALUES ('1', '1', '北京三里屯', '北京中关村', '2016-11-01');





--------------------------------------------------------------------------------------------------------

/*
Navicat MySQL Data Transfer

Source Server         : localhost_3306
Source Server Version : 50129
Source Host           : localhost:3306
Source Database       : test

Target Server Type    : MYSQL
Target Server Version : 50129
File Encoding         : 65001

Date: 2016-11-08 13:52:48
*/

SET FOREIGN_KEY_CHECKS=0;

-- ----------------------------
-- Table structure for `bicycle`
-- ----------------------------
DROP TABLE IF EXISTS `bicycle`;
CREATE TABLE `bicycle` (
  `bicid` int(10) NOT NULL,
  `begin` varchar(50) NOT NULL,
  `end` varchar(50) NOT NULL,
  PRIMARY KEY (`bicid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of bicycle
-- ----------------------------
INSERT INTO `bicycle` VALUES ('1', '北京三里屯', '北京中关村');
