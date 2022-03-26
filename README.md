-- phpMyAdmin SQL Dump
-- version 5.0.4
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: Mar 14, 2021 at 11:10 AM
-- Server version: 10.4.17-MariaDB
-- PHP Version: 8.0.2
SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";
/*!40101 SET
@OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET
@OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET
@OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;
--
-- Database: `lifeblood`
--
-- -------------------------------------------------------
-
--
-- Table structure for table `admin`
--
CREATE TABLE `admin` (
 `id` int(11) NOT NULL,
 `username` varchar(100) NOT NULL,
 `password` varchar(100) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
--
33
-- Dumping data for table `admin`
--
INSERT INTO `admin` (`id`, `username`, `password`) VALUES
(1, 'admin', '10fe97a829eb7830aba87656c1e2b85d');
-- -------------------------------------------------------
-
--
-- Table structure for table `bank`
--
CREATE TABLE `bank` (
 `id` int(11) NOT NULL,
 `name` text NOT NULL,
 `contact` text NOT NULL,
 `address` varchar(30) NOT NULL,
 `status` varchar(30) DEFAULT 'Not Verified'
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
--
-- Dumping data for table `bank`
--
INSERT INTO `bank` (`id`, `name`, `contact`, `address`,
`status`) VALUES
(1, 'Aditya Blood Bank', '040 24763565', 'Abids,
Hyderabad', 'Verified'),
(2, 'Aarohi Blood Bank', '040 65742923', 'Banjara Hills,
Hyderabad', 'Verified'),
(3, 'Red Cross Blood Bank', '040 27633087', 'Vidya Nagar,
Hyderabad', 'Verified'),
(4, 'Vivekananda Blood Bank', '7947447569', 'Mehdipatnam,
Hyderabad', 'Verified'),
(5, 'Prasad Hospital Blood Bank', '7947060035', 'Nacharam,
Hyderabad', 'Verified'),
(6, 'Janani Voluntary Blood Bank', '8045792510', 'Kphp,
Hyderabad', 'Not Verified'),
(7, 'Ymca Blood Bank', '040 23226624', 'Narayanagua,
Hyderabad', 'Not Verified');
-- -------------------------------------------------------
-
34
--
-- Table structure for table `donor`
--
CREATE TABLE `donor` (
 `id` int(11) NOT NULL,
 `name` text NOT NULL,
 `email` text NOT NULL,
 `contact` varchar(20) NOT NULL,
 `address` varchar(30) NOT NULL,
 `gender` text NOT NULL,
 `blood` varchar(30) NOT NULL,
 `health` varchar(30) NOT NULL,
 `status` varchar(30) DEFAULT 'Not Approved'
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
--
-- Dumping data for table `donor`
--
INSERT INTO `donor` (`id`, `name`, `email`, `contact`,
`address`, `gender`, `blood`, `health`, `status`) VALUES
(0, 'donor01', 'donor01@gmail.com', '8848550101', 'Abids,
Hyd', 'male', 'O+', 'yes', 'Approved'),
(1, 'donor02', 'donor02@gmail.com', '8848550102', 'Koti,
Hyd', 'Male', 'A+', 'No', 'Approved'),
(2, 'donor03', 'donor03@gmail.com', '8848550103',
'Kacheguda, Hyd', 'Female', 'A-', 'Yes', 'Pending'),
(3, 'donor04', 'donor04@gmail.com', '8848550104',
'Secundrabad, Hyd', 'Female', 'B+', 'Yes', 'Not
Approved'),
(4, 'donor05', 'donor05@gmail.com', '8848550105',
'Chikadpally, Hyd', 'Male', 'B+', 'No', 'Not Approved');
-- -------------------------------------------------------
-
--
-- Table structure for table `seeker`
--
CREATE TABLE `seeker` (
 `id` int(11) NOT NULL,
35
 `name` text NOT NULL,
 `email` text NOT NULL,
 `contact` varchar(20) NOT NULL,
 `address` varchar(30) NOT NULL,
 `gender` text NOT NULL,
 `blood` varchar(30) NOT NULL,
 `hospital` varchar(50) NOT NULL,
 `purpose` varchar(30) NOT NULL,
 `status` varchar(30) DEFAULT 'Not Approved'
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
--
-- Dumping data for table `seeker`
--
INSERT INTO `seeker` (`id`, `name`, `email`, `contact`,
`address`, `gender`, `blood`, `hospital`, `purpose`,
`status`) VALUES
(0, 'seeker01', 'seeker01@gmail.com', '9956568501',
'Abids, Hyd', 'Female', 'A+', 'Apollo, DRDO', 'Surgery',
'Approved'),
(1, 'seeker02', 'seeker02@gmail.com', '9956568502',
'Nampally, Hyd', 'Male', 'A+', 'Care, Nampally',
'Surgery', 'Approved'),
(2, 'seeker03', 'seeker03@gmail.com', '9956568503',
'Nalgonda X Road, Hyd', 'Male', 'B+', 'Nims, Panjagutta',
'Surgery', 'Pending'),
(3, 'seeker04', 'seeker04@gmail.com', '9956568504', 'Afzal
Gunj, Hyd', 'Female', 'O+', 'Virinchi, Banjara Hills',
'Surgery', 'Not Approved'),
(4, 'seeker05', 'seeker05@gmail.com', '9956568505', 'Zoo
Park, Hyd', 'Male', 'O+', 'Owaisi, Pisalbanda', 'Surgery',
'Not Approved');
-- -------------------------------------------------------
-
--
-- Table structure for table `users`
--
CREATE TABLE `users` (
 `id` int(11) NOT NULL,
 `username` varchar(100) NOT NULL,
36
 `email` varchar(100) NOT NULL,
 `password` varchar(100) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
--
-- Dumping data for table `users`
--
INSERT INTO `users` (`id`, `username`, `email`,
`password`) VALUES
(8, 'User', 'User.lifeblood@gmail.com',
'd2cfb9b7fda81e06c50b12f9ce550f62');
--
-- Indexes for dumped tables
--
--
-- Indexes for table `admin`
--
ALTER TABLE `admin`
 ADD PRIMARY KEY (`id`);
--
-- Indexes for table `bank`
--
ALTER TABLE `bank`
 ADD PRIMARY KEY (`id`);
--
-- Indexes for table `donor`
--
ALTER TABLE `donor`
 ADD PRIMARY KEY (`id`);
--
-- Indexes for table `seeker`
--
ALTER TABLE `seeker`
 ADD PRIMARY KEY (`id`);
--
-- Indexes for table `users`
--
37
ALTER TABLE `users`
 ADD PRIMARY KEY (`id`);
--
-- AUTO_INCREMENT for dumped tables
--
--
-- AUTO_INCREMENT for table `users`
--
ALTER TABLE `users`
 MODIFY `id` int(11) NOT NULL AUTO_INCREMENT,
AUTO_INCREMENT=9;
COMMIT;
/*!40101 SET
CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET
CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET
COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
